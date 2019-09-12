----------------------------- Enabling PITest to the existing project------------------
            <plugin>
                <groupId>org.pitest</groupId>
                <artifactId>pitest-maven</artifactId>
                <version>1.4.0</version>
                <dependencies>
                    <dependency>
                        <groupId>org.pitest</groupId>
                        <artifactId>pitest-junit5-plugin</artifactId>
                        <version>0.5</version>
                    </dependency>
                </dependencies>
             </plugin>

---------------------------------------------------------------------------------------

-----------------------------Specifying/Ignoring the classes for PITest -----------------------------
<!--<configuration>
    <targetClasses>
        <param>com.example.swcoe.reward.*</param>
    </targetClasses>
</configuration>—>
--------------------------------------------------------------------------------------------------------------------

-----------------------------Enabling Mutators/groups----------------------------------------------------------
                <configuration>
                    <targetClasses>
                        <param>com.example.swcoe.reward.*</param>
                    </targetClasses>
			        <mutators>
			            <!-- <mutator>DEFAULTS</mutator> -->
				        <!-- <mutator>STRONGER</mutator> -->
				        <mutator>ALL</mutator>
				    </mutators>
                </configuration>
--------------------------------------------------------------------------------------------------------------------

-----------------------------Report Generation type ----------------------------------------------------------
                <configuration>
                    <targetClasses>
                        <param>com.example.swcoe.reward.*</param>
                    </targetClasses>
			        <reportsDirectory>
				        ${project.build.directory}/mutation-reports
				    </reportsDirectory>
				    <outputFormats>
					    <value>XML</value>
					    <value>HTML</value>
						<value>CSV</value>
					</outputFormats>
					<timestampedReports>false</timestampedReports>
                </configuration>
-------------------------------------------------------------------------------------------------------------------------------------------------

-----------------------------Running only modified files---------------------------------------------------------------------------------------

                <configuration>
                    <targetClasses>
			            <param>com.example.swcoe.reward*</param>
			        </targetClasses>
			        <historyInputFile>${project.basedir}/history.bin</historyInputFile>
    				<historyOutputFile>${project.basedir}/history.bin</historyOutputFile>
			    </configuration>
-------------------------------------------------------------------------------------------------------------------------------------------------                



                
