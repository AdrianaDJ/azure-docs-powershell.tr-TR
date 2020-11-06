---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Save-AzureRmDataFactoryLog.md
ms.openlocfilehash: 8525333f2be148b59053c62fc4d0f95dda8949a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592237"
---
# <span data-ttu-id="00614-101">Save-AzureRmDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="00614-101">Save-AzureRmDataFactoryLog</span></span>

## <span data-ttu-id="00614-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00614-102">SYNOPSIS</span></span>
<span data-ttu-id="00614-103">Azure HDInsight işlemeden günlük dosyalarını indirir.</span><span class="sxs-lookup"><span data-stu-id="00614-103">Downloads log files from Azure HDInsight processing.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00614-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00614-104">SYNTAX</span></span>

### <span data-ttu-id="00614-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="00614-105">ByFactoryName (Default)</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00614-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="00614-106">ByFactoryObject</span></span>
```
Save-AzureRmDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00614-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="00614-107">DESCRIPTION</span></span>
<span data-ttu-id="00614-108">**Save-AzureRmDataFactoryLog** cmdlet 'ı, domuz veya kovan projelerinin Azure HDInsight işlemeyle ilişkili günlük dosyalarını veya özel etkinlikleri yerel sabit sürücünüze indirir.</span><span class="sxs-lookup"><span data-stu-id="00614-108">The **Save-AzureRmDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="00614-109">İlk olarak, bir veri dilimi için bir etkinliğin KIMLIĞINI almak üzere Get-AzureRmDataFactoryRun cmdlet 'i çalıştırırsınız ve ardından bu KIMLIĞI kullanarak, HDInsight kümesiyle ilişkili ikili büyük nesne (BLOB) depolama alanından günlük dosyalarını alırsınız.</span><span class="sxs-lookup"><span data-stu-id="00614-109">You first run the Get-AzureRmDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>

<span data-ttu-id="00614-110">*Downloadlogs* parametresini belirtmezseniz, cmdlet yalnızca günlük dosyalarının konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="00614-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>

<span data-ttu-id="00614-111">Bir çıkış dizini ( *Çıkış* parametresi) belirtmeden *downloadlogs* belirtirseniz, günlük dosyaları varsayılan belgeler klasörüne indirilir.</span><span class="sxs-lookup"><span data-stu-id="00614-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>

<span data-ttu-id="00614-112">Bir çıkış klasörüyle ( *Çıkış* ) birlikte *downloadlogs günlükleri* belirtirseniz, günlük dosyaları belirtilen klasöre indirilir.</span><span class="sxs-lookup"><span data-stu-id="00614-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="00614-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00614-113">EXAMPLES</span></span>

### <span data-ttu-id="00614-114">Örnek 1: günlük dosyalarını belirli bir klasöre kaydetme</span><span class="sxs-lookup"><span data-stu-id="00614-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="00614-115">Bu komut, etkinliğin günlük dosyalarını, etkinliğin, ADF adlı kaynak grubundaki Logprocessingname adlı Data Factory adındaki bir ardışık düzene ait 841b77c9-d56c-48D1-99a3-8c16c3e77d39 KIMLIĞIYLE çalışır.</span><span class="sxs-lookup"><span data-stu-id="00614-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="00614-116">Günlük dosyaları C:\Test klasörüne kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="00614-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="00614-117">Örnek 2: günlük dosyalarını varsayılan belgeler klasörüne kaydetme</span><span class="sxs-lookup"><span data-stu-id="00614-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="00614-118">Bu komut günlük dosyalarını Belgeler klasörüne kaydeder (varsayılan).</span><span class="sxs-lookup"><span data-stu-id="00614-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="00614-119">Örnek 3: günlük dosyalarının konumunu alma</span><span class="sxs-lookup"><span data-stu-id="00614-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzureRmDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="00614-120">Bu komut, günlük dosyalarının konumunu döndürür.</span><span class="sxs-lookup"><span data-stu-id="00614-120">This command returns the location of log files.</span></span>
<span data-ttu-id="00614-121">*Downloadlogs* 'un belirtilmemiştir.</span><span class="sxs-lookup"><span data-stu-id="00614-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="00614-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00614-122">PARAMETERS</span></span>

### <span data-ttu-id="00614-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="00614-123">-DataFactory</span></span>
<span data-ttu-id="00614-124">**Psdatafactory** nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00614-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="00614-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="00614-125">-DataFactoryName</span></span>
<span data-ttu-id="00614-126">Veri Fabrikası adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00614-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="00614-127">Bu cmdlet, bu parametrenin belirttiği veri fabrikası için günlük dosyalarını indirir.</span><span class="sxs-lookup"><span data-stu-id="00614-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="00614-128">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="00614-128">-DownloadLogs</span></span>
<span data-ttu-id="00614-129">Bu cmdlet 'in günlük dosyalarını yerel bilgisayarınıza indirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="00614-129">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="00614-130">*Ouptut* klasörü belirtilmezse, dosyalar alt klasörün altındaki Belgeler klasörüne kaydedilir.</span><span class="sxs-lookup"><span data-stu-id="00614-130">If *Ouptut* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="00614-131">-ID</span><span class="sxs-lookup"><span data-stu-id="00614-131">-Id</span></span>
<span data-ttu-id="00614-132">Veri dilimi için etkinliğin çalışma KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="00614-132">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="00614-133">KIMLIK almak için Get-AzureRmDataFactoryRun cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="00614-133">Use the Get-AzureRmDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="00614-134">-Çıktı</span><span class="sxs-lookup"><span data-stu-id="00614-134">-Output</span></span>
<span data-ttu-id="00614-135">İndirilen günlük dosyalarının kaydedildiği çıkış klasörünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="00614-135">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="00614-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00614-136">-ResourceGroupName</span></span>
<span data-ttu-id="00614-137">Bir Azure Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00614-137">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="00614-138">Bu cmdlet, bu parametrenin belirttiği gruba ait bir veri fabrikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="00614-138">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="00614-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00614-139">-DefaultProfile</span></span>
<span data-ttu-id="00614-140">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="00614-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00614-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00614-141">CommonParameters</span></span>
<span data-ttu-id="00614-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00614-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00614-143">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00614-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00614-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00614-144">INPUTS</span></span>

## <span data-ttu-id="00614-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00614-145">OUTPUTS</span></span>

### <span data-ttu-id="00614-146">Microsoft. Azure. Commands. DataFactory. modeller. Psrunlogınfo</span><span class="sxs-lookup"><span data-stu-id="00614-146">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="00614-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00614-147">NOTES</span></span>
* <span data-ttu-id="00614-148">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="00614-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="00614-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00614-149">RELATED LINKS</span></span>

[<span data-ttu-id="00614-150">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="00614-150">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="00614-151">Get-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="00614-151">Get-AzureRmDataFactoryPipeline</span></span>](./Get-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="00614-152">Yeni-Azurermdatafactorypeline</span><span class="sxs-lookup"><span data-stu-id="00614-152">New-AzureRmDataFactoryPipeline</span></span>](./New-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="00614-153">Remove-Azurermdatafactorypda</span><span class="sxs-lookup"><span data-stu-id="00614-153">Remove-AzureRmDataFactoryPipeline</span></span>](./Remove-AzureRmDataFactoryPipeline.md)

[<span data-ttu-id="00614-154">Set-Azurermdatafactoryptam</span><span class="sxs-lookup"><span data-stu-id="00614-154">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="00614-155">Askıya al-Azurermdatafactorypla</span><span class="sxs-lookup"><span data-stu-id="00614-155">Suspend-AzureRmDataFactoryPipeline</span></span>](./Suspend-AzureRmDataFactoryPipeline.md)


