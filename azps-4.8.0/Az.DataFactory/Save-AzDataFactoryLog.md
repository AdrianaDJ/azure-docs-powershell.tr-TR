---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: cf1e0738a01d2b8f3219f2732995182fe7f6959d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268003"
---
# <span data-ttu-id="a23f3-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="a23f3-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="a23f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a23f3-102">SYNOPSIS</span></span>
<span data-ttu-id="a23f3-103">Azure HDInsight işlemeden günlük dosyalarını indirir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="a23f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a23f3-104">SYNTAX</span></span>

### <span data-ttu-id="a23f3-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a23f3-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a23f3-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="a23f3-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a23f3-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a23f3-107">DESCRIPTION</span></span>
<span data-ttu-id="a23f3-108">**Save-AzDataFactoryLog** cmdlet 'ı, domuz veya Hive projelerinin Azure HDInsight işlemeyle ilişkili günlük dosyalarını veya özel etkinlikleri yerel sabit sürücünüze indirir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="a23f3-109">İlk olarak, bir veri dilimi için bir etkinliğin KIMLIĞINI almak üzere Get-AzDataFactoryRun cmdlet 'i çalıştırırsınız ve ardından bu KIMLIĞI kullanarak, HDInsight kümesiyle ilişkili ikili büyük nesne (BLOB) depolama alanından günlük dosyalarını alırsınız.</span><span class="sxs-lookup"><span data-stu-id="a23f3-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="a23f3-110">*Downloadlogs* parametresini belirtmezseniz, cmdlet yalnızca günlük dosyalarının konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a23f3-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="a23f3-111">Bir çıkış dizini ( *Çıkış* parametresi) belirtmeden *downloadlogs* belirtirseniz, günlük dosyaları varsayılan belgeler klasörüne indirilir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="a23f3-112">Bir çıkış klasörüyle ( *Çıkış* ) birlikte *downloadlogs günlükleri* belirtirseniz, günlük dosyaları belirtilen klasöre indirilir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="a23f3-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a23f3-113">EXAMPLES</span></span>

### <span data-ttu-id="a23f3-114">Örnek 1: günlük dosyalarını belirli bir klasöre kaydetme</span><span class="sxs-lookup"><span data-stu-id="a23f3-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="a23f3-115">Bu komut, etkinliğin günlük dosyalarını, etkinliğin, ADF adlı kaynak grubundaki Logprocessingname adlı Data Factory adındaki bir ardışık düzene ait 841b77c9-d56c-48D1-99a3-8c16c3e77d39 KIMLIĞIYLE çalışır.</span><span class="sxs-lookup"><span data-stu-id="a23f3-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="a23f3-116">Günlük dosyaları C:\Test klasörüne kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="a23f3-117">Örnek 2: günlük dosyalarını varsayılan belgeler klasörüne kaydetme</span><span class="sxs-lookup"><span data-stu-id="a23f3-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="a23f3-118">Bu komut günlük dosyalarını Belgeler klasörüne kaydeder (varsayılan).</span><span class="sxs-lookup"><span data-stu-id="a23f3-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="a23f3-119">Örnek 3: günlük dosyalarının konumunu alma</span><span class="sxs-lookup"><span data-stu-id="a23f3-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="a23f3-120">Bu komut, günlük dosyalarının konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="a23f3-120">This command returns the location of log files.</span></span>
<span data-ttu-id="a23f3-121">*Downloadlogs* 'un belirtilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="a23f3-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a23f3-122">PARAMETERS</span></span>

### <span data-ttu-id="a23f3-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="a23f3-123">-DataFactory</span></span>
<span data-ttu-id="a23f3-124">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-124">Specifies a **PSDataFactory** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23f3-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a23f3-125">-DataFactoryName</span></span>
<span data-ttu-id="a23f3-126">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="a23f3-127">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için günlük dosyalarını indirir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23f3-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a23f3-128">-DefaultProfile</span></span>
<span data-ttu-id="a23f3-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a23f3-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a23f3-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="a23f3-130">-DownloadLogs</span></span>
<span data-ttu-id="a23f3-131">Bu cmdlet 'in günlük dosyalarını yerel bilgisayarınıza indirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="a23f3-132">*Çıkış* klasörü belirtilmezse, dosyalar alt klasörün altındaki Belgeler klasörüne kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a23f3-133">-ID</span><span class="sxs-lookup"><span data-stu-id="a23f3-133">-Id</span></span>
<span data-ttu-id="a23f3-134">Veri dilimi için etkinliğin çalışma KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="a23f3-135">KIMLIK almak için Get-AzDataFactoryRun cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="a23f3-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23f3-136">-Çıktı</span><span class="sxs-lookup"><span data-stu-id="a23f3-136">-Output</span></span>
<span data-ttu-id="a23f3-137">İndirilen günlük dosyalarının kaydedildiği çıkış klasörünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a23f3-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a23f3-138">-ResourceGroupName</span></span>
<span data-ttu-id="a23f3-139">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a23f3-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a23f3-140">Bu cmdlet, bu parametrenin belirttiği gruba ait bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a23f3-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a23f3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a23f3-141">CommonParameters</span></span>
<span data-ttu-id="a23f3-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a23f3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a23f3-143">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a23f3-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a23f3-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a23f3-144">INPUTS</span></span>

### <span data-ttu-id="a23f3-145">Microsoft.Azure.Commands.DataFactories.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="a23f3-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="a23f3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a23f3-146">System.String</span></span>

## <span data-ttu-id="a23f3-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a23f3-147">OUTPUTS</span></span>

### <span data-ttu-id="a23f3-148">Microsoft. Azure. Commands. DataFactory. modeller. Psrunlogınfo</span><span class="sxs-lookup"><span data-stu-id="a23f3-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="a23f3-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a23f3-149">NOTES</span></span>
* <span data-ttu-id="a23f3-150">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="a23f3-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a23f3-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a23f3-151">RELATED LINKS</span></span>

[<span data-ttu-id="a23f3-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="a23f3-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="a23f3-153">Get-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="a23f3-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="a23f3-154">Yeni-Azveri Factorypya</span><span class="sxs-lookup"><span data-stu-id="a23f3-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="a23f3-155">Remove-Azdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="a23f3-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="a23f3-156">Set-Azdatafactorypipelineactivedönem</span><span class="sxs-lookup"><span data-stu-id="a23f3-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="a23f3-157">Askıya al-Azverfactorypya</span><span class="sxs-lookup"><span data-stu-id="a23f3-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


