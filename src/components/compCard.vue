<template>
  <theme-provider :theme="{
    primary :'palevioletred'
  }">
  <Wrapper>
    <StyledTitle>
      스타일 컴포넌트
    </StyledTitle>
    <styled-button>Normal</styled-button>
    <styled-button primary>Primary</styled-button>

  </Wrapper>
  </theme-provider>
</template>

<script>
import styled from "vue-styled-components";
import {StyledTitle} from './style';
import {ThemeProvider} from 'vue-styled-components';


const Wrapper = styled.section`
  padding:4em;
  background:${props => props.theme.primary};
`


const btnProps = {primary : Boolean};

const StyledButton = styled('button', btnProps)`
  ont-size: 1em;
  margin: 1em;
  padding: 0.25em 1em;
  border: 2px solid palevioletred;
  border-radius: 3px;
  background:${props => props.primary ? 'palevioletred' : 'white'};
  color: ${props => props.primary ? 'white' : 'palevioletred'};
`

export default {
  name: 'compCard',
  components:{
    Wrapper,
    StyledTitle,
    StyledButton,
    'theme-provider' : ThemeProvider,
  },
  props:{
    propA : String,
    propB : [String, Number]
  }
};
</script>
