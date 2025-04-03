<template>
    <div class="calculator bg-light">
      <div class="display">{{ display }}</div>
      <div class="row g-2">
        <div class="col-3">
          <button class="btn btn-secondary btn-custom" @click="clear">C</button>
        </div>
        <div class="col-3">
          <button class="btn btn-secondary btn-custom" @click="append('(')">(</button>
        </div>
        <div class="col-3">
          <button class="btn btn-secondary btn-custom" @click="append(')')">)</button>
        </div>
        <div class="col-3">
          <button class="btn btn-warning btn-custom" @click="operation('/')">/</button>
        </div>
  
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('7')">7</button>
        </div>
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('8')">8</button>
        </div>
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('9')">9</button>
        </div>
        <div class="col-3">
          <button class="btn btn-warning btn-custom" @click="operation('*')">×</button>
        </div>
  
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('4')">4</button>
        </div>
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('5')">5</button>
        </div>
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('6')">6</button>
        </div>
        <div class="col-3">
          <button class="btn btn-warning btn-custom" @click="operation('-')">-</button>
        </div>
  
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('1')">1</button>
        </div>
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('2')">2</button>
        </div>
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('3')">3</button>
        </div>
        <div class="col-3">
          <button class="btn btn-warning btn-custom" @click="operation('+')">+</button>
        </div>
  
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('0')">0</button>
        </div>
        <div class="col-3">
          <button class="btn btn-primary btn-custom" @click="append('.')">.</button>
        </div>
        <div class="col-6">
          <button class="btn btn-success btn-custom" @click="calculate">=</button>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Calculadora',
    data() {
      return {
        display: '0'
      };
    },
    methods: {
      append(value) {
        if (this.display === '0' && value !== '.') {
          this.display = value;
        } else {
          this.display += value;
        }
      },
      operation(op) {
        this.display += ` ${op} `;
      },
      clear() {
        this.display = '0';
      },
      calculate() {
        try {
          this.display = eval(this.display).toString();
        } catch (e) {
          this.display = 'Error';
          setTimeout(() => this.clear(), 1000);
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .calculator {
    max-width: 400px;
    margin: 50px auto;
    padding: 20px;
    border-radius: 10px;
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.1);
  }
  
  .display {
    font-size: 2rem;
    padding: 15px;
    background-color: #f8f9fa;
    border-radius: 5px;
    text-align: right;
    margin-bottom: 20px;
  }
  
  .btn-custom {
    font-size: 1.2rem;
    padding: 15px;
    width: 100%;
  }
  </style>