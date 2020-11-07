---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: fdf8d4fefef434e503c0fc21c3036577e56b56c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752572"
---
# <span data-ttu-id="7b493-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="7b493-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="7b493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b493-102">SYNOPSIS</span></span>
<span data-ttu-id="7b493-103">Veri akışı kaynağı ve bağımlılıklarını belirli veri akışı hata ayıklama oturumuna ekleyin.</span><span class="sxs-lookup"><span data-stu-id="7b493-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="7b493-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7b493-104">SYNTAX</span></span>

### <span data-ttu-id="7b493-105">ByFactoryName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7b493-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b493-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7b493-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b493-107">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="7b493-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b493-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="7b493-108">DESCRIPTION</span></span>
<span data-ttu-id="7b493-109">Bu komut veri akışı kaynağını ve bağımlılıklarını belirli bir hata ayıklama oturumuna iliştirir veri akışı hata ayıklama iş akışı için PowerShell komut dizisi şöyle olmalıdır:</span><span class="sxs-lookup"><span data-stu-id="7b493-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="7b493-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7b493-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="7b493-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="7b493-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="7b493-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (Bu adımı farklı komutlar/hedefler için tekrarlama veya paket dosyasını değiştirmek için 2-3 adımını tekrarlama)</span><span class="sxs-lookup"><span data-stu-id="7b493-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="7b493-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7b493-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="7b493-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7b493-114">EXAMPLES</span></span>

### <span data-ttu-id="7b493-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7b493-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="7b493-116">"W50effe4-93a3-485C-8525-eaf25259efbd"/"WikiADF" Veri Fabrikası</span><span class="sxs-lookup"><span data-stu-id="7b493-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="7b493-117">Pakcage dosyası veri akışı hata ayıklama kaynağı, veri kümesi hata ayıklama kaynağının listesi, bağlantılı hizmet hata ayıklama kaynağı listesi, hata ayıklama ayarı ve oturum KIMLIĞI içerir.</span><span class="sxs-lookup"><span data-stu-id="7b493-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="7b493-118">Örneğin:</span><span class="sxs-lookup"><span data-stu-id="7b493-118">For instance:</span></span>

<span data-ttu-id="7b493-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName = ad; AccountKey = anahtar; EndpointSuffix = Core. Windows. net "}}}]," debugSettings ": {" sourceSettings ": [{" sourceName ":" source1 "," rowLimit ": 1000}]," SessionID ":" 4f988caf-e765-47vseç2-82cd-430334a6b135 "}</span><span class="sxs-lookup"><span data-stu-id="7b493-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="7b493-120">SessionID parametresi, paket dosyasındaki var olan SessionID özelliğini değiştirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="7b493-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="7b493-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7b493-121">PARAMETERS</span></span>

### <span data-ttu-id="7b493-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7b493-122">-DataFactory</span></span>
<span data-ttu-id="7b493-123">Veri fabrikası nesnesi.</span><span class="sxs-lookup"><span data-stu-id="7b493-123">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b493-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="7b493-124">-DataFactoryName</span></span>
<span data-ttu-id="7b493-125">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="7b493-125">The data factory name.</span></span>

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

### <span data-ttu-id="7b493-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b493-126">-DefaultProfile</span></span>
<span data-ttu-id="7b493-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7b493-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b493-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="7b493-128">-PackageFile</span></span>
<span data-ttu-id="7b493-129">JSON dosyası yolu.</span><span class="sxs-lookup"><span data-stu-id="7b493-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b493-130">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7b493-130">-PassThru</span></span>
<span data-ttu-id="7b493-131">Belirtilirse, çalışması işlemi başarılı olduğunda doğru yazılır.</span><span class="sxs-lookup"><span data-stu-id="7b493-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="7b493-132">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="7b493-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b493-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b493-133">-ResourceGroupName</span></span>
<span data-ttu-id="7b493-134">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7b493-134">The resource group name.</span></span>

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

### <span data-ttu-id="7b493-135">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7b493-135">-ResourceId</span></span>
<span data-ttu-id="7b493-136">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="7b493-136">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b493-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="7b493-137">-Confirm</span></span>
<span data-ttu-id="7b493-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="7b493-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b493-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b493-139">-WhatIf</span></span>
<span data-ttu-id="7b493-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7b493-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b493-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="7b493-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b493-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b493-142">CommonParameters</span></span>
<span data-ttu-id="7b493-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7b493-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b493-144">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7b493-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b493-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7b493-145">INPUTS</span></span>

### <span data-ttu-id="7b493-146">System. String</span><span class="sxs-lookup"><span data-stu-id="7b493-146">System.String</span></span>

### <span data-ttu-id="7b493-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDAtafabrikası</span><span class="sxs-lookup"><span data-stu-id="7b493-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="7b493-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7b493-148">OUTPUTS</span></span>

### <span data-ttu-id="7b493-149">System. void</span><span class="sxs-lookup"><span data-stu-id="7b493-149">System.Void</span></span>

### <span data-ttu-id="7b493-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b493-150">System.Boolean</span></span>

## <span data-ttu-id="7b493-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7b493-151">NOTES</span></span>
<span data-ttu-id="7b493-152">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrikalar</span><span class="sxs-lookup"><span data-stu-id="7b493-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7b493-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7b493-153">RELATED LINKS</span></span>

[<span data-ttu-id="7b493-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7b493-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="7b493-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7b493-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="7b493-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="7b493-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="7b493-157">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="7b493-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)