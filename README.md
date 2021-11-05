# Fun-With-Layout
Deuxieme rapport de KEBDANI Mohamed Amine et TOUIHAME Rania
<!DOCTYPE html>
<html>
  <head>
    
  </head>
  <body>
    <h2 class="post-title">Programming Widget Layout</h2>
    <h3>Experimenting with QHBOXLayout</h3>
    <p>First , we &nbsp;wanted to create a basic project called <strong>hbox&nbsp;</strong>with the following code:</p>
    <pre style='color:#d1d1d1;background:#000000;'><span style='color:#e66170; font-weight:bold; '>int</span> <span style='color:#e66170; font-weight:bold; '>main</span><span style='color:#d2cd86; '>(</span><span style='color:#e66170; font-weight:bold; '>int</span> argc<span style='color:#d2cd86; '>,</span> <span style='color:#e66170; font-weight:bold; '>char</span><span style='color:#d2cd86; '>*</span> argv<span style='color:#d2cd86; '>[</span><span style='color:#d2cd86; '>]</span><span style='color:#d2cd86; '>)</span>
<span style='color:#b060b0; '>{</span>
  <span style='color:#e66170; font-weight:bold; '>QApplication</span> app<span style='color:#d2cd86; '>(</span>argc<span style='color:#d2cd86; '>,</span> argv<span style='color:#d2cd86; '>)</span><span style='color:#b060b0; '>;</span>

  <span style='color:#e66170; font-weight:bold; '>QWidget</span><span style='color:#d2cd86; '>*</span> window <span style='color:#d2cd86; '>=</span> <span style='color:#e66170; font-weight:bold; '>new</span> <span style='color:#e66170; font-weight:bold; '>QWidget</span><span style='color:#d2cd86; '>(</span><span style='color:#d2cd86; '>)</span><span style='color:#b060b0; '>;</span>
  window<span style='color:#d2cd86; '>-</span><span style='color:#d2cd86; '>></span>setWindowTitle<span style='color:#d2cd86; '>(</span><span style='color:#02d045; '>"</span><span style='color:#00c4c4; '>QHBoxLayout Test</span><span style='color:#02d045; '>"</span><span style='color:#d2cd86; '>)</span><span style='color:#b060b0; '>;</span>

  window<span style='color:#d2cd86; '>-</span><span style='color:#d2cd86; '>></span>show<span style='color:#d2cd86; '>(</span><span style='color:#d2cd86; '>)</span><span style='color:#b060b0; '>;</span>

  <span style='color:#e66170; font-weight:bold; '>return</span> app<span style='color:#d2cd86; '>.</span>exec<span style='color:#d2cd86; '>(</span><span style='color:#d2cd86; '>)</span><span style='color:#b060b0; '>;</span>
<span style='color:#b060b0; '>}</span>
</pre>
<p>And presente the following window:</p>

![hbox window](https://user-images.githubusercontent.com/93485000/140558586-6e652e86-60b3-41a0-a48f-3064ee2035ff.png)

<p>Basically all of our component are placed horizentally, so that&apos;s why we&apos;ll only use the <strong>QHBoxLayout.</strong></p>
<p>So our work was the following:</p>
 <!-- ---------------------------------------------------------------------------------------------------------------------------------------------- -->
<p>For the hbox's header file dialog1.h:</p>
    
<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">ifndef</span><span style="color:#008073; "> DIALOG1_H</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">define</span><span style="color:#008073; "> DIALOG1_H</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QWidget</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLabel</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLineEdit</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QPushButton</span><span style="color:#02d045; ">&gt;</span>

<span style="color:#e66170; font-weight:bold; ">class</span> Dialog1<span style="color:#b060b0; ">:</span> <span style="color:#e66170; font-weight:bold; ">public</span> <span style="color:#e66170; font-weight:bold; ">QWidget</span>
<span style="color:#b060b0; ">{</span>
<span style="color:#e66170; font-weight:bold; ">public</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">explicit</span> Dialog1<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">QWidget</span> <span style="color:#d2cd86; ">*</span>parent<span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">nullptr</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

<span style="color:#e66170; font-weight:bold; ">protected</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> createWidgets<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> placeWidgets<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> makeConnexions<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

<span style="color:#e66170; font-weight:bold; ">protected</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span><span style="color:#e66170; font-weight:bold; ">search</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>name<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLineEdit</span> <span style="color:#d2cd86; ">*</span>edit<span style="color:#b060b0; ">;</span>


<span style="color:#b060b0; ">}</span><span style="color:#b060b0; ">;</span>


<span style="color:#008073; ">#</span><span style="color:#008073; ">endif</span><span style="color:#008073; "> </span><span style="color:#9999a9; ">// DIALOG1_H</span>
</pre>
<!--------------------------------------------------------------------------------------------------------------------------------------------------------->
<p>Hbox's source file dialog1.cpp:</p>
    
<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">"</span><span style="color:#40015a; ">dialog1.h</span><span style="color:#02d045; ">"</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QHBoxLayout</span><span style="color:#02d045; ">&gt;</span>

Dialog1<span style="color:#b060b0; ">::</span>Dialog1<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">QWidget</span> <span style="color:#d2cd86; ">*</span>parent<span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>

    <span style="color:#9999a9; ">//etape 1</span>
    createWidgets<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


    <span style="color:#9999a9; ">//etape 2</span>
    placeWidgets<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//etape3</span>
    makeConnexions<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>

<span style="color:#e66170; font-weight:bold; ">void</span> Dialog1<span style="color:#b060b0; ">::</span>createWidgets<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>
    name<span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Name</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    edit <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLineEdit</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">search</span> <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Search</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>


<span style="color:#e66170; font-weight:bold; ">void</span> Dialog1<span style="color:#b060b0; ">::</span>placeWidgets<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>

    <span style="color:#e66170; font-weight:bold; ">auto</span> layout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">this</span><span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>setLayout<span style="color:#d2cd86; ">(</span>layout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


    <span style="color:#9999a9; ">//ajouter les layouts</span>
    layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>name<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>edit<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">search</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

<span style="color:#b060b0; ">}</span>

<span style="color:#e66170; font-weight:bold; ">void</span> Dialog1<span style="color:#b060b0; ">::</span>makeConnexions<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>

<span style="color:#b060b0; ">}</span>
</pre>
 <!-------------------------------------------------------------------------------------------------------------------------------------------------------------------->
<p>And for the hbox's main.cpp:</p>
    
<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QApplication</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QWidget</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QHBoxLayout</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QPushButton</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLineEdit</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLabel</span><span style="color:#02d045; ">&gt;</span>

<span style="color:#e66170; font-weight:bold; ">int</span> <span style="color:#e66170; font-weight:bold; ">main</span><span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">int</span> argc<span style="color:#d2cd86; ">,</span> <span style="color:#e66170; font-weight:bold; ">char</span> <span style="color:#d2cd86; ">*</span>argv<span style="color:#d2cd86; ">[</span><span style="color:#d2cd86; ">]</span><span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>
    <span style="color:#9999a9; ">//creation de l'application</span>
    <span style="color:#e66170; font-weight:bold; ">QApplication</span> app<span style="color:#d2cd86; ">(</span>argc<span style="color:#d2cd86; ">,</span> argv<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//creation du layout horizontal</span>
    <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span> <span style="color:#d2cd86; ">*</span>layout<span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//creation d'une fenetre</span>
    <span style="color:#e66170; font-weight:bold; ">QWidget</span> <span style="color:#d2cd86; ">*</span>window <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QWidget</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//creation du label "name"</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>namelabel<span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Name :</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">,</span> window<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//creation input part</span>
    <span style="color:#e66170; font-weight:bold; ">QLineEdit</span> <span style="color:#d2cd86; ">*</span>text<span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLineEdit</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//creation du button "search"</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>searchbutton<span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Search</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">,</span> window<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>namelabel<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>text<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>searchbutton<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//indiquer que le titre de cette page sera "QHBoxLayout Test"</span>
     window<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>setWindowTitle<span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">QHBoxLayout Test</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

     window<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>setLayout<span style="color:#d2cd86; ">(</span>layout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
     window<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>show<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">return</span> app<span style="color:#d2cd86; ">.</span>exec<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>
</pre>
 
<!-------------------------------------------------------------------------------------------------------------------------------------------------------------->

<p>So our window appear as follow:</p>   
    
![hbox tp](https://user-images.githubusercontent.com/93485000/140558691-c3fbd9c2-b4d8-4e56-ae1e-a314e4381eeb.png)

   
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------->
<h3>Nested Layouts</h3>
<p>The goal of the exercice is to analyse the construction of a form and then code it using <strong>Netsted layouts</strong>. </p>
<p>The aim of this exercice is to avoid coding any <strong>functinality</strong>, just the form of the dialog. </p>
    
![nested layout window](https://user-images.githubusercontent.com/93485000/140548025-8f25d7d1-8b10-4340-90e5-22105a4d219c.png)
<!-------------------------------------------------------------------------------------------------------------------------------------->
<p>In order to add a layout to a main one, we&rsquo;ll have to use&nbsp; : &nbsp; </p>
<p>The Widget with a empty checkable <strong>square</strong> is a <a href="https://doc.qt.io/qt-5/qcheckbox.html">QCheckBox</a>. </p>
    
<p>So our nested layout&apos;s header dialog2.h is:</p>

<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">ifndef</span><span style="color:#008073; "> DIALOG2_H</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">define</span><span style="color:#008073; "> DIALOG2_H</span>

<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QWidget</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QPushButton</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLabel</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QCheckBox</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLineEdit</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QSpacerItem</span><span style="color:#02d045; ">&gt;</span>


<span style="color:#e66170; font-weight:bold; ">class</span> Dialog2 <span style="color:#b060b0; ">:</span> <span style="color:#e66170; font-weight:bold; ">public</span> <span style="color:#e66170; font-weight:bold; ">QWidget</span>
<span style="color:#b060b0; ">{</span>

<span style="color:#e66170; font-weight:bold; ">public</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">explicit</span> Dialog2<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">QWidget</span> <span style="color:#d2cd86; ">*</span>parent <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">nullptr</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">virtual</span> <span style="color:#d2cd86; ">~</span>Dialog2<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#e66170; font-weight:bold; ">protected</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> creatWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> placeWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> makeConnexion<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#9999a9; ">//    void creatVLayout();</span>
<span style="color:#9999a9; ">//    void creatHLayout();</span>
<span style="color:#9999a9; ">//    void placeVLayout();</span>
<span style="color:#9999a9; ">//    void placeHLayout();</span>

<span style="color:#e66170; font-weight:bold; ">protected</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>name<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLineEdit</span> <span style="color:#d2cd86; ">*</span>inputname<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span><span style="color:#e66170; font-weight:bold; ">search</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>close<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QCheckBox</span> <span style="color:#d2cd86; ">*</span>check1<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QCheckBox</span> <span style="color:#d2cd86; ">*</span>check2<span style="color:#b060b0; ">;</span>


<span style="color:#b060b0; ">}</span><span style="color:#b060b0; ">;</span>

<span style="color:#008073; ">#</span><span style="color:#008073; ">endif</span><span style="color:#008073; "> </span><span style="color:#9999a9; ">// DIALOG2_H</span>

</pre>
<!------------------------------------------------------------------------------------------------------------------------------------------------------------------->
<p>The source file dialog2.cpp is :</p>

<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">"</span><span style="color:#40015a; ">dialog2.h</span><span style="color:#02d045; ">"</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QApplication</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QWidget</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QPushButton</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLabel</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QCheckBox</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLineEdit</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QSpacerItem</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QHBoxLayout</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QVBoxLayout</span><span style="color:#02d045; ">&gt;</span>


Dialog2<span style="color:#b060b0; ">::</span>Dialog2<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">QWidget</span> <span style="color:#d2cd86; ">*</span>parent<span style="color:#d2cd86; ">)</span> <span style="color:#b060b0; ">:</span> <span style="color:#e66170; font-weight:bold; ">QWidget</span><span style="color:#d2cd86; ">(</span>parent<span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>

    <span style="color:#9999a9; ">//etape 1</span>
    creatWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


    <span style="color:#9999a9; ">//etape2</span>
    placeWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//etape 3</span>
    <span style="color:#9999a9; ">//creatHLayout();</span>


    <span style="color:#9999a9; ">//etape 4</span>
   <span style="color:#9999a9; ">// creatVLayout();</span>


    <span style="color:#9999a9; ">//etape 5</span>
    <span style="color:#9999a9; ">// placeHLayout();</span>


    <span style="color:#9999a9; ">//placeVLayout();</span>



    <span style="color:#9999a9; ">//etape 6</span>
    makeConnexion<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>


Dialog2<span style="color:#b060b0; ">::</span><span style="color:#d2cd86; ">~</span>Dialog2<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> name<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> inputname<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> <span style="color:#e66170; font-weight:bold; ">search</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> close<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> check1<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> check2<span style="color:#b060b0; ">;</span>



<span style="color:#b060b0; ">}</span>


<span style="color:#e66170; font-weight:bold; ">void</span> Dialog2<span style="color:#b060b0; ">::</span>creatWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>
    name <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Name</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    inputname<span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLineEdit</span><span style="color:#b060b0; ">;</span>
    check1 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QCheckBox</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Search Backward</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    check2 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QCheckBox</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Match case</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">search</span> <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Search</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    close <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Close</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


<span style="color:#b060b0; ">}</span>

<span style="color:#e66170; font-weight:bold; ">void</span> Dialog2<span style="color:#b060b0; ">::</span>makeConnexion<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>
    <span style="color:#e66170; font-weight:bold; ">connect</span><span style="color:#d2cd86; ">(</span>close<span style="color:#d2cd86; ">,</span> <span style="color:#d2cd86; ">&amp;</span><span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#b060b0; ">::</span>clicked<span style="color:#d2cd86; ">,</span>qApp<span style="color:#d2cd86; ">,</span> <span style="color:#d2cd86; ">&amp;</span><span style="color:#e66170; font-weight:bold; ">QApplication</span><span style="color:#b060b0; ">::</span><span style="color:#e66170; font-weight:bold; ">exit</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>

<span style="color:#e66170; font-weight:bold; ">void</span> Dialog2<span style="color:#b060b0; ">::</span>placeWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>
    <span style="color:#9999a9; ">//layouts principaux</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> mainLayout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> rightLayout <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QVBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> leftLayout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QVBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> leftUpLayout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    setLayout<span style="color:#d2cd86; ">(</span>mainLayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>



    <span style="color:#9999a9; ">//meta structuration</span>
    mainLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>leftLayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    mainLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>rightLayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    leftLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>leftUpLayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


    <span style="color:#9999a9; ">//contenu de chaque layout</span>
    leftUpLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>name<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    leftUpLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>inputname<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//terminer la partie left</span>
    leftLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>check1<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    leftLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>check2<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


    <span style="color:#9999a9; ">//terminer le rightlayout</span>
    rightLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">search</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    rightLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>close<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    rightLayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addSpacerItem<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QSpacerItem</span><span style="color:#d2cd86; ">(</span><span style="color:#008c00; ">10</span><span style="color:#d2cd86; ">,</span> <span style="color:#008c00; ">10</span> <span style="color:#d2cd86; ">,</span><span style="color:#e66170; font-weight:bold; ">QSizePolicy</span><span style="color:#b060b0; ">::</span>Expanding<span style="color:#d2cd86; ">)</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


<span style="color:#b060b0; ">}</span>

</pre>
<!------------------------------------------------------------------------------------------------------------------------------------------------------------>
<p>And the main.cpp file is :</p>

<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QApplication</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">"</span><span style="color:#40015a; ">dialog2.h</span><span style="color:#02d045; ">"</span>

<span style="color:#e66170; font-weight:bold; ">int</span> <span style="color:#e66170; font-weight:bold; ">main</span><span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">int</span> argc<span style="color:#d2cd86; ">,</span> <span style="color:#e66170; font-weight:bold; ">char</span> <span style="color:#d2cd86; ">*</span>argv<span style="color:#d2cd86; ">[</span><span style="color:#d2cd86; ">]</span><span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>
    <span style="color:#e66170; font-weight:bold; ">QApplication</span> app<span style="color:#d2cd86; ">(</span>argc<span style="color:#d2cd86; ">,</span> argv<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    Dialog2 <span style="color:#d2cd86; ">*</span>d<span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> Dialog2<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    d<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>show<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">return</span> app<span style="color:#d2cd86; ">.</span>exec<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>
</pre>
<!------------------------------------------------------------------------------------------------------------------------------------------------------------->
<p>So our windon came up as follow :</p>

![nested layout window tp](https://user-images.githubusercontent.com/93485000/140550910-5483aae3-48cf-47cc-9a8b-cd97a7d649df.png)
 <!---------------------------------------------------------------------------------------------------------------------------------------------------->

<h3>Bug report Form</h3>
<p>Our task is to create the following form to report a problem .</p>
    
![Bug report form window](https://user-images.githubusercontent.com/93485000/140551925-cdcc6c83-f948-410e-990c-caa3ad5ce659.png)

<!----------------------------------------------------------------------------------------------------------------------------------------------------------------------->
<p>In this exercice, we just had to use all the tools that we just saw previouslly.</p>
<p>For the Bug report form&apos;s header file dialog3.h :</p>

<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">ifndef</span><span style="color:#008073; "> DIALOG3_H</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">define</span><span style="color:#008073; "> DIALOG3_H</span>

<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QWidget</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QPushButton</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLabel</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLineEdit</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QTextEdit</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QSpacerItem</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QMenuBar</span><span style="color:#02d045; ">&gt;</span>

<span style="color:#e66170; font-weight:bold; ">class</span> Dialog3 <span style="color:#b060b0; ">:</span> <span style="color:#e66170; font-weight:bold; ">public</span> <span style="color:#e66170; font-weight:bold; ">QWidget</span>
<span style="color:#b060b0; ">{</span>

<span style="color:#e66170; font-weight:bold; ">public</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">explicit</span> Dialog3<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">QWidget</span> <span style="color:#d2cd86; ">*</span>parent <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">nullptr</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">virtual</span> <span style="color:#d2cd86; ">~</span>Dialog3<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#e66170; font-weight:bold; ">protected</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> creatWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> placeWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   <span style="color:#9999a9; ">// void makeConnexion();</span>

<span style="color:#e66170; font-weight:bold; ">protected</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>name<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>company<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>phone<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>email<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>probtitle<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>suminfo<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLabel</span> <span style="color:#d2cd86; ">*</span>reproducibility<span style="color:#b060b0; ">;</span>

    <span style="color:#e66170; font-weight:bold; ">QLineEdit</span> <span style="color:#d2cd86; ">*</span>inpname<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLineEdit</span> <span style="color:#d2cd86; ">*</span>inpcompany<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLineEdit</span> <span style="color:#d2cd86; ">*</span>inpphone<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLineEdit</span> <span style="color:#d2cd86; ">*</span>inpemail<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QLineEdit</span> <span style="color:#d2cd86; ">*</span>inpprobtitle<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QTextEdit</span> <span style="color:#d2cd86; ">*</span>inpsuminfo<span style="color:#b060b0; ">;</span>

    <span style="color:#e66170; font-weight:bold; ">QLineEdit</span> <span style="color:#d2cd86; ">*</span>inpreproducibility<span style="color:#b060b0; ">;</span>

    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>reset<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>subbugrep<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>dontsub<span style="color:#b060b0; ">;</span>



<span style="color:#b060b0; ">}</span><span style="color:#b060b0; ">;</span>

<span style="color:#008073; ">#</span><span style="color:#008073; ">endif</span><span style="color:#008073; "> </span><span style="color:#9999a9; ">// DIALOG3_H</span>
</pre>
<!--------------------------------------------------------------------------------------------------------------------------------------------------------------->
    
<p>Concerning the source file dialog3.cpp, we tried to write it the most easy way so that we lower the odds of error.</p>

<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">"</span><span style="color:#40015a; ">dialog3.h</span><span style="color:#02d045; ">"</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QApplication</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QWidget</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QPushButton</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLabel</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QCheckBox</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLineEdit</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QSpacerItem</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QHBoxLayout</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QVBoxLayout</span><span style="color:#02d045; ">&gt;</span>

Dialog3<span style="color:#b060b0; ">::</span>Dialog3<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">QWidget</span> <span style="color:#d2cd86; ">*</span>parent<span style="color:#d2cd86; ">)</span> <span style="color:#b060b0; ">:</span> <span style="color:#e66170; font-weight:bold; ">QWidget</span><span style="color:#d2cd86; ">(</span>parent<span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>
    <span style="color:#9999a9; ">//etape1</span>
    creatWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//etape2</span>
    placeWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    <span style="color:#9999a9; ">//etape3</span>
    <span style="color:#9999a9; ">//makeConnexion();</span>

<span style="color:#b060b0; ">}</span>

Dialog3<span style="color:#b060b0; ">::</span><span style="color:#d2cd86; ">~</span>Dialog3<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> name<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> company<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> phone<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> email<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> probtitle<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> suminfo<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> reproducibility<span style="color:#b060b0; ">;</span>

    <span style="color:#e66170; font-weight:bold; ">delete</span> inpname<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> inpcompany<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> inpphone<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> inpemail<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> inpprobtitle<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> inpsuminfo<span style="color:#b060b0; ">;</span>

    <span style="color:#e66170; font-weight:bold; ">delete</span> inpreproducibility<span style="color:#b060b0; ">;</span>

    <span style="color:#e66170; font-weight:bold; ">delete</span> reset<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> subbugrep<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> dontsub<span style="color:#b060b0; ">;</span>


<span style="color:#b060b0; ">}</span>

<span style="color:#e66170; font-weight:bold; ">void</span> Dialog3<span style="color:#b060b0; ">::</span>creatWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>
    name <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Name :</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    company <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Company :</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    phone <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Phone :</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    email <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Email :</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    probtitle <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Probtitle :</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    suminfo <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Summary Information :</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    reproducibility <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLabel</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Reproducibility :</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    inpname <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLineEdit</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    inpcompany <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLineEdit</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    inpphone <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLineEdit</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    inpemail <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLineEdit</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    inpprobtitle <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLineEdit</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    inpsuminfo <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QTextEdit</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    inpreproducibility <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLineEdit</span><span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    reset <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Reset</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    subbugrep <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Submit Bug Report</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    dontsub <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Don't Submit</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>




<span style="color:#b060b0; ">}</span>


<span style="color:#e66170; font-weight:bold; ">void</span> Dialog3<span style="color:#b060b0; ">::</span>placeWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> mainlayout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QVBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> namelayout <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> companylayout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> phonelayout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> emaillayout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> probtitlelayout<span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> suminfolayout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> reproducibilitylayout <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">auto</span> buttonslayout <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QHBoxLayout</span><span style="color:#b060b0; ">;</span>
    setLayout<span style="color:#d2cd86; ">(</span>mainlayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


    namelayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>name<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    namelayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>inpname<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    companylayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>company<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    companylayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>inpcompany<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    phonelayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>phone<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    phonelayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>inpphone<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    emaillayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>email<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    emaillayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>inpemail<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


    probtitlelayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>probtitle<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    probtitlelayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>inpprobtitle<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    suminfolayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>suminfo<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    suminfolayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>inpsuminfo<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


    reproducibilitylayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>reproducibility<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    reproducibilitylayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>inpreproducibility<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    buttonslayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>reset<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    buttonslayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addSpacerItem<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QSpacerItem</span><span style="color:#d2cd86; ">(</span><span style="color:#008c00; ">10</span><span style="color:#d2cd86; ">,</span> <span style="color:#008c00; ">10</span> <span style="color:#d2cd86; ">,</span><span style="color:#e66170; font-weight:bold; ">QSizePolicy</span><span style="color:#b060b0; ">::</span>Expanding<span style="color:#d2cd86; ">)</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    buttonslayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>subbugrep<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    buttonslayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>dontsub<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>namelayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>companylayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>phonelayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>emaillayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>probtitlelayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>suminfolayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>reproducibilitylayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>buttonslayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>




<span style="color:#b060b0; ">}</span>

</pre>
  <!-------------------------------------------------------------------------------------------------------------------------------------------------------------->
    
<p>And for the main.cpp file , it&apos;s pretty the same as the previous exercices:</p>

<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QApplication</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">"</span><span style="color:#40015a; ">dialog3.h</span><span style="color:#02d045; ">"</span>


<span style="color:#e66170; font-weight:bold; ">int</span> <span style="color:#e66170; font-weight:bold; ">main</span><span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">int</span> argc<span style="color:#d2cd86; ">,</span> <span style="color:#e66170; font-weight:bold; ">char</span> <span style="color:#d2cd86; ">*</span>argv<span style="color:#d2cd86; ">[</span><span style="color:#d2cd86; ">]</span><span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>
    <span style="color:#e66170; font-weight:bold; ">QApplication</span> app<span style="color:#d2cd86; ">(</span>argc<span style="color:#d2cd86; ">,</span> argv<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    Dialog3 <span style="color:#d2cd86; ">*</span>d3<span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">new</span> Dialog3<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    d3<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>show<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">return</span> app<span style="color:#d2cd86; ">.</span>exec<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>
</pre>
<!-------------------------------------------------------------------------------------------------------------------------------------------------------------->
 <p>So our window came up as follow :</p>
  
 ![Bug report form tp](https://user-images.githubusercontent.com/93485000/140554497-07deb456-b487-4efc-860d-b4ed8835c76f.png)
    
<!--------------------------------------------------------------------------------------------------------------------------------------------------------->
<h3>Grid Layout</h3>
<p>Last but not least, we have to construct the following calculator using the <a href="https://doc.qt.io/qt-5.15/qgridlayout.html">QGridLayout</a> :</p>
    
![grid layout window](https://user-images.githubusercontent.com/93485000/140555663-14cb9284-d3ad-4a57-a90e-b6311ceaa5b5.png)
    
<!------------------------------------------------------------------------------------------------------------------------------------------------------>
<p>In this exercice we used a new component that shows the number called a <a href="https://doc.qt.io/archives/qt-4.8/qlcdnumber.html">LCDNumber</a>. </p>
<p>The grid layout&apos;s header file dialog4.h is :</p>

<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">ifndef</span><span style="color:#008073; "> DIALOG4_H</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">define</span><span style="color:#008073; "> DIALOG4_H</span>

<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QGridLayout</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLCDNumber</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QPushButton</span><span style="color:#02d045; ">&gt;</span>


<span style="color:#e66170; font-weight:bold; ">class</span> Dialog4 <span style="color:#b060b0; ">:</span> <span style="color:#e66170; font-weight:bold; ">public</span> <span style="color:#e66170; font-weight:bold; ">QWidget</span>
<span style="color:#b060b0; ">{</span>

<span style="color:#e66170; font-weight:bold; ">public</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">explicit</span> Dialog4<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">QWidget</span> <span style="color:#d2cd86; ">*</span>parent <span style="color:#d2cd86; ">=</span> <span style="color:#e66170; font-weight:bold; ">nullptr</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#e66170; font-weight:bold; ">protected</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> creatWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> placeWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> makeConnexion<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">void</span> setMinimumHeight<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">virtual</span> <span style="color:#d2cd86; ">~</span>Dialog4<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#e66170; font-weight:bold; ">protected</span><span style="color:#e34adc; ">:</span>
    <span style="color:#e66170; font-weight:bold; ">QLCDNumber</span> <span style="color:#d2cd86; ">*</span>inpnumber<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button0<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button1<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button2<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button3<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button4<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button5<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button6<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button7<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button8<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>button9<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">QPushButton</span> <span style="color:#d2cd86; ">*</span>enterbutton<span style="color:#b060b0; ">;</span>



<span style="color:#b060b0; ">}</span><span style="color:#b060b0; ">;</span>

<span style="color:#008073; ">#</span><span style="color:#008073; ">endif</span><span style="color:#008073; "> </span><span style="color:#9999a9; ">// DIALOG4_H</span>
</pre>
<!---------------------------------------------------------------------------------------------------------------------------------------------------------------------->
    
 <p>The source file dialog4.cpp is :</p>
 
<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">"</span><span style="color:#40015a; ">dialog4.h</span><span style="color:#02d045; ">"</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QGridLayout</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QPushButton</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QLCDNumber</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QWidget</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QBoxLayout</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QVBoxLayout</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QApplication</span><span style="color:#02d045; ">&gt;</span>

Dialog4<span style="color:#b060b0; ">::</span>Dialog4<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">QWidget</span> <span style="color:#d2cd86; ">*</span>parent<span style="color:#d2cd86; ">)</span> <span style="color:#b060b0; ">:</span> <span style="color:#e66170; font-weight:bold; ">QWidget</span><span style="color:#d2cd86; ">(</span>parent<span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>
    creatWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    placeWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    makeConnexion<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>

    setMinimumHeight<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


<span style="color:#b060b0; ">}</span>

Dialog4<span style="color:#b060b0; ">::</span><span style="color:#d2cd86; ">~</span>Dialog4<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> inpnumber<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button0<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button1<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button2<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button3<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button4<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button5<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button6<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button7<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button8<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> button9<span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">delete</span> enterbutton<span style="color:#b060b0; ">;</span>

<span style="color:#b060b0; ">}</span>

<span style="color:#e66170; font-weight:bold; ">void</span> Dialog4<span style="color:#b060b0; ">::</span>creatWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>

    inpnumber <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QLCDNumber</span><span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">this</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    inpnumber<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>setDigitCount<span style="color:#d2cd86; ">(</span><span style="color:#008c00; ">6</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>


    button0 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">0</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    button1 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">1</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    button2 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">2</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    button3 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">3</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    button4 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">4</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    button5 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">5</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    button6 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">6</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    button7 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">7</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    button8 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">8</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    button9 <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">9</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    enterbutton <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QPushButton</span><span style="color:#d2cd86; ">(</span><span style="color:#02d045; ">"</span><span style="color:#00c4c4; ">Enter</span><span style="color:#02d045; ">"</span><span style="color:#d2cd86; ">,</span><span style="color:#e66170; font-weight:bold; ">this</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    enterbutton<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>setSizePolicy<span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">QSizePolicy</span><span style="color:#b060b0; ">::</span>Expanding<span style="color:#d2cd86; ">,</span> <span style="color:#e66170; font-weight:bold; ">QSizePolicy</span><span style="color:#b060b0; ">::</span>Fixed<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    enterbutton<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>resize<span style="color:#d2cd86; ">(</span>sizeHint<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#d2cd86; ">.</span>width<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#d2cd86; ">,</span> sizeHint<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#d2cd86; ">.</span>height<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>




<span style="color:#b060b0; ">}</span>
<span style="color:#e66170; font-weight:bold; ">void</span> Dialog4<span style="color:#b060b0; ">::</span>placeWidget<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>
   <span style="color:#e66170; font-weight:bold; ">auto</span> mainlayout <span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QVBoxLayout</span><span style="color:#b060b0; ">;</span>
   <span style="color:#e66170; font-weight:bold; ">auto</span> layout<span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> <span style="color:#e66170; font-weight:bold; ">QGridLayout</span><span style="color:#b060b0; ">;</span>
   setLayout<span style="color:#d2cd86; ">(</span>mainlayout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>inpnumber<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button0<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">4</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">0</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button1<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">3</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">0</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button2<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">3</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">1</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button3<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">3</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">2</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button4<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">2</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">0</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button5<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">2</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">1</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button6<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">2</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">2</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button7<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">1</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">0</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button8<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">1</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">1</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>button9<span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">1</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">2</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   layout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addWidget<span style="color:#d2cd86; ">(</span>enterbutton<span style="color:#d2cd86; ">,</span> <span style="color:#008c00; ">4</span><span style="color:#d2cd86; ">,</span> <span style="color:#008c00; ">1</span><span style="color:#d2cd86; ">,</span> <span style="color:#008c00; ">1</span><span style="color:#d2cd86; ">,</span><span style="color:#008c00; ">2</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
   mainlayout<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>addLayout<span style="color:#d2cd86; ">(</span>layout<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>


<span style="color:#e66170; font-weight:bold; ">void</span> Dialog4<span style="color:#b060b0; ">::</span>makeConnexion<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>

<span style="color:#9999a9; ">//    connect(button0, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>
<span style="color:#9999a9; ">//    connect(button1, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>
<span style="color:#9999a9; ">//    connect(button2, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>
<span style="color:#9999a9; ">//    connect(button3, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>
<span style="color:#9999a9; ">//    connect(button4, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>
<span style="color:#9999a9; ">//    connect(button5, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>
<span style="color:#9999a9; ">//    connect(button6, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>
<span style="color:#9999a9; ">//    connect(button7, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>
<span style="color:#9999a9; ">//    connect(button8, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>
<span style="color:#9999a9; ">//    connect(button9, &amp;QPushButton::clicked,qApp, &amp;QLCDNumber::);</span>

<span style="color:#b060b0; ">}</span>

<span style="color:#e66170; font-weight:bold; ">void</span> Dialog4<span style="color:#b060b0; ">::</span>setMinimumHeight<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">{</span>

   inpnumber<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>setMinimumHeight<span style="color:#d2cd86; ">(</span><span style="color:#008c00; ">8</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>

</pre>
    
    
 <!--------------------------------------------------------------------------------------------------------------------------------------------->
 <p>The main.cpp as i previously said, stay the same : </p>
 
<pre style="color:#d1d1d1;background:#000000;"><span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QApplication</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">&lt;</span><span style="color:#40015a; ">QWidget</span><span style="color:#02d045; ">&gt;</span>
<span style="color:#008073; ">#</span><span style="color:#008073; ">include </span><span style="color:#02d045; ">"</span><span style="color:#40015a; ">dialog4.h</span><span style="color:#02d045; ">"</span>

<span style="color:#e66170; font-weight:bold; ">int</span> <span style="color:#e66170; font-weight:bold; ">main</span><span style="color:#d2cd86; ">(</span><span style="color:#e66170; font-weight:bold; ">int</span> argc<span style="color:#d2cd86; ">,</span> <span style="color:#e66170; font-weight:bold; ">char</span> <span style="color:#d2cd86; ">*</span>argv<span style="color:#d2cd86; ">[</span><span style="color:#d2cd86; ">]</span><span style="color:#d2cd86; ">)</span>
<span style="color:#b060b0; ">{</span>
    <span style="color:#e66170; font-weight:bold; ">QApplication</span> app<span style="color:#d2cd86; ">(</span>argc<span style="color:#d2cd86; ">,</span> argv<span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    Dialog4 <span style="color:#d2cd86; ">*</span>d<span style="color:#d2cd86; ">=</span><span style="color:#e66170; font-weight:bold; ">new</span> Dialog4<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    d<span style="color:#d2cd86; ">-</span><span style="color:#d2cd86; ">&gt;</span>show<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
    <span style="color:#e66170; font-weight:bold; ">return</span> app<span style="color:#d2cd86; ">.</span>exec<span style="color:#d2cd86; ">(</span><span style="color:#d2cd86; ">)</span><span style="color:#b060b0; ">;</span>
<span style="color:#b060b0; ">}</span>
</pre>
<!-------------------------------------------------------------------------------------------------->
<p>So our window ended up like this :</p>
 
![grid layout tp](https://user-images.githubusercontent.com/93485000/140558247-3feb5a75-2593-477e-b445-89ddd0121c5e.png)

   
   
  

    
       
    
  </body>
</html>
