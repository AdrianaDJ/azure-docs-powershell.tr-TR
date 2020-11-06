---
Module Name: AzureRM.HDInsight
Module Guid: 3fd1475f-cb23-4ffb-bf08-33d94b7d1acb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight
Help Version: 4.1.2.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/AzureRM.HDInsight.md
ms.openlocfilehash: ed52eb21cfa5d192e4d7d0d79a2dc0847a5fd3ee
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93570625"
---
# AzureRM. HDInsight modülü
## Tanım
Bu bölümdeki konular, Azure Resource Manager (ARM) çerçevesindeki Microsoft Azure HDInsight için Azure PowerShell cmdlet 'lerini belgeleyin. Bu cmdlet 'ler HDInsight kümelerini ve bunların üzerinde çalışan işleri yönetmek için kullanılır. Microsoft. Azure. Commands. HDInsight ad alanında cmdlet 'ler vardır.

## AzureRM. HDInsight cmdlet 'Leri
### [Add-AzureRmHDInsightClusterIdentity](Add-AzureRmHDInsightClusterIdentity.md)
Küme yapılandırma nesnesine küme kimliği ekler.

### [Add-AzureRmHDInsightComponentVersion](Add-AzureRmHDInsightComponentVersion.md)
Kümede çalışan bir hizmetin bir kopyasını küme yapılandırma nesnesine ekler.

### [Add-AzureRmHDInsightConfigValues](Add-AzureRmHDInsightConfigValues.md)
Bir küme yapılandırma nesnesine bir Hadoop yapılandırma değeri özelleştirmesi ve/veya kovan Paylaşılan kitaplık özelleştirmesi ekler.

### [Add-AzureRmHDInsightMetastore](Add-AzureRmHDInsightMetastore.md)
Bir SQL veritabanını yığın veya Oozie metaser olarak bir küme yapılandırma nesnesine ekler.

### [Add-AzureRmHDInsightScriptAction](Add-AzureRmHDInsightScriptAction.md)
Küme yapılandırma nesnesine bir komut dosyası eylemi ekler.

### [Add-AzureRmHDInsightSecurityProfile](Add-AzureRmHDInsightSecurityProfile.md)
Küme yapılandırma nesnesine bir güvenlik profilimi ekler.

### [Add-AzureRmHDInsightStorage](Add-AzureRmHDInsightStorage.md)
Küme yapılandırma nesnesine Azure depolama anahtarı ekler.

### [Disable-AzureRmHDInsightOperationsManagementSuite](Disable-AzureRmHDInsightOperationsManagementSuite.md)
Bir HDInsight kümesindeki Operations Management paketini (OMS) devre dışı bırakır ve ilgili Günlükler, etkinleştir sırasında belirtilen OMS çalışma alanına akışını durdurur.

### [Enable-AzureRmHDInsightOperationsManagementSuite](Enable-AzureRmHDInsightOperationsManagementSuite.md)
Bir HDInsight kümesinde Operations Management Suite (OMS) özelliğini etkinleştirir ve ilgili Günlükler etkinleştir sırasında belirtilen OMS çalışma alanına gönderilir.

### [Get-AzureRmHDInsightCluster](Get-AzureRmHDInsightCluster.md)
Geçerli abonelikle ilişkilendirilmiş tüm Azure HDInsight kümelerini veya belirli bir kaynak grubunu alır ve listeler.

### [Get-AzureRmHDInsightJob](Get-AzureRmHDInsightJob.md)
Bir kümeden işlerin listesini alır ve bunları ters sırada listeler veya belirli bir iş alır.

### [Get-AzureRmHDInsightJobOutput](Get-AzureRmHDInsightJobOutput.md)
Belirli bir kümeyle ilişkilendirilmiş depolama hesabından bir işin günlük çıkışını alır.

### [Get-AzureRmHDInsightOperationsManagementSuite](Get-AzureRmHDInsightOperationsManagementSuite.md)
Kümedeki Operations Management Suite (OMS) yüklemesinin durumunu alır.

### [Get-AzureRmHDInsightPersistedScriptAction](Get-AzureRmHDInsightPersistedScriptAction.md)
Kümenin kalıcı komut dosyası eylemlerini alır ve bunları kronolojik sırada listeler veya belirli bir kalıcı betik eyleminin ayrıntılarını alır.

### [Get-AzureRmHDInsightProperties](Get-AzureRmHDInsightProperties.md)
HDInsight hizmeti hakkında, kullanılabilir konumlar ve kapasite gibi özellikleri alır.

### [Get-AzureRmHDInsightScriptActionHistory](Get-AzureRmHDInsightScriptActionHistory.md)
Kümenin komut dosyası eylem geçmişini alır ve ters kronolojik sırayla listeler veya önceden çalıştırılmış bir betik eyleminin ayrıntılarını alır.

### [Grant-AzureRmHDInsightHttpServicesAccess](Grant-AzureRmHDInsightHttpServicesAccess.md)
Kümeye HTTP erişimi verir.

### [Grant-AzureRmHDInsightRdpServicesAccess](Grant-AzureRmHDInsightRdpServicesAccess.md)
Windows kümesine RDP erişimi verir.

### [Invoke-AzureRmHDInsightHiveJob](Invoke-AzureRmHDInsightHiveJob.md)
Bir HDInsight kümesine kovan sorgusu gönderir ve sorgu sonuçlarını tek bir işlemde alır.

### [New-AzureRmHDInsightCluster](New-AzureRmHDInsightCluster.md)
Geçerli abonelik için belirtilen kaynak grubunda bir Azure HDInsight kümesi oluşturur.

### [New-AzureRmHDInsightClusterConfig](New-AzureRmHDInsightClusterConfig.md)
Azure HDInsight küme yapılandırmasını tanımlayan kalıcı olmayan bir küme yapılandırma nesnesi oluşturur.

### [New-AzureRmHDInsightHiveJobDefinition](New-AzureRmHDInsightHiveJobDefinition.md)
Bir kovan iş nesnesi oluşturur.

### [New-AzureRmHDInsightMapReduceJobDefinition](New-AzureRmHDInsightMapReduceJobDefinition.md)
MapReduce iş nesnesi oluşturur.

### [New-AzureRmHDInsightPigJobDefinition](New-AzureRmHDInsightPigJobDefinition.md)
Domuz iş nesnesi oluşturur.

### [New-AzureRmHDInsightSqoopJobDefinition](New-AzureRmHDInsightSqoopJobDefinition.md)
Bir Sqoop iş nesnesi oluşturur.

### [New-AzureRmHDInsightStreamingMapReduceJobDefinition](New-AzureRmHDInsightStreamingMapReduceJobDefinition.md)
Bir akış MapReduce iş nesnesi oluşturur.

### [Remove-AzureRmHDInsightCluster](Remove-AzureRmHDInsightCluster.md)
Belirtilen HDInsight kümesini geçerli abonelikten kaldırır.

### [Remove-AzureRmHDInsightPersistedScriptAction](Remove-AzureRmHDInsightPersistedScriptAction.md)
Bir HDInsight kümesinden kalıcı betik eylemini kaldırır.

### [Revoke-AzureRmHDInsightHttpServicesAccess](Revoke-AzureRmHDInsightHttpServicesAccess.md)
Kümeye HTTP erişimini devre dışı bırakır.

### [Revoke-AzureRmHDInsightRdpServicesAccess](Revoke-AzureRmHDInsightRdpServicesAccess.md)
Windows kümesine RDP erişimini devre dışı bırakır.

### [Set-AzureRmHDInsightClusterSize](Set-AzureRmHDInsightClusterSize.md)
Belirtilen kümede çalışan düğümü sayısını ayarlar.

### [Set-AzureRmHDInsightDefaultStorage](Set-AzureRmHDInsightDefaultStorage.md)
Küme yapılandırma nesnesindeki varsayılan depolama hesabı ayarını ayarlar.

### [Set-AzureRmHDInsightPersistedScriptAction](Set-AzureRmHDInsightPersistedScriptAction.md)
Önceden çalıştırılmış bir betik eylemini kalıcı bir betik eylemi olarak ayarlar.

### [Start-AzureRmHDInsightJob](Start-AzureRmHDInsightJob.md)
Belirtilen bir kümede tanımlı Azure HDInsight işini başlatır.

### [Stop-AzureRmHDInsightJob](Stop-AzureRmHDInsightJob.md)
Kümede belirtilen çalışan işi durdurur.

### [Submit-AzureRmHDInsightScriptAction](Submit-AzureRmHDInsightScriptAction.md)
Bir Azure HDInsight kümesine yeni bir betik eylemi gönderir.

### [Use-AzureRmHDInsightCluster](Use-AzureRmHDInsightCluster.md)
Invoke-RmAzureHDInsightHiveJob cmdlet 'inde kullanılacak kümeyi seçer.

### [Bekle-AzureRmHDInsightJob](Wait-AzureRmHDInsightJob.md)
Belirtilen işin tamamlanmasını veya başarısızlığını bekler.

