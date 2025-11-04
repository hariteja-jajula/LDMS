

<pre class=" language-markdown"><code class="prism  language-markdown"><span class="token title important"><span class="token punctuation">#</span> LDMS Sampler Quick Demo</span>

<span class="token title important"><span class="token punctuation">###</span> 1. Set environment</span>
```bash
export LDMS<span class="token italic"><span class="token punctuation">_</span>HOME=/root/ldms-install
export PATH=$LDMS<span class="token punctuation">_</span></span>HOME/sbin:$LDMS<span class="token italic"><span class="token punctuation">_</span>HOME/bin:$PATH
export LD<span class="token punctuation">_</span></span>LIBRARY<span class="token italic"><span class="token punctuation">_</span>PATH=$LDMS<span class="token punctuation">_</span></span>HOME/lib:$LD<span class="token italic"><span class="token punctuation">_</span>LIBRARY<span class="token punctuation">_</span></span>PATH

</code></pre>
<h3 id="start-sampler">2. Start sampler</h3>
<pre class=" language-bash"><code class="prism  language-bash">ldmsd -v INFO -c <span class="token variable">$LDMS_HOME</span>/ldmsd.conf

</code></pre>
<h3 id="in-another-terminal-connect-and-view-metrics">3. In another terminal, connect and view metrics</h3>
<pre class=" language-bash"><code class="prism  language-bash">ldms_ls -x sock -p 10000
ldms_ls -x sock -p 10000 -l

</code></pre>
<h3 id="optional-save-a-few-samples">4. (Optional) Save a few samples</h3>
<pre class=" language-bash"><code class="prism  language-bash">ldms_cstat -x sock -p 10000 -a csv -o samples.csv -t 5

</code></pre>
<hr>

