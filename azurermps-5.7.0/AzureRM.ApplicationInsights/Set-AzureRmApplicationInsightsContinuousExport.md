---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/set-azurermapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/Set-AzureRmApplicationInsightsContinuousExport.md
ms.openlocfilehash: 7b426f7f6b494c92d86a41217000b2d2335c7d91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593520"
---
# <span data-ttu-id="78983-101">Set-AzureRmApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="78983-101">Set-AzureRmApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="78983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78983-102">SYNOPSIS</span></span>
<span data-ttu-id="78983-103">Applcıation Insights kaynağında sürekli dışarı aktarma yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="78983-103">Update a continuous export configuration in an applciation insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78983-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="78983-104">SYNTAX</span></span>

### <span data-ttu-id="78983-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="78983-105">ComponentNameParameterSet (Default)</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78983-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="78983-106">ComponentObjectParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 -ExportId <String> -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String>
 -StorageSASUri <String> [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78983-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="78983-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmApplicationInsightsContinuousExport [-ResourceId] <String> -ExportId <String>
 -DocumentType <String[]> -StorageAccountId <String> -StorageLocation <String> -StorageSASUri <String>
 [-DisableConfiguration] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78983-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="78983-108">DESCRIPTION</span></span>
<span data-ttu-id="78983-109">Applcıation Insights kaynağında sürekli dışarı aktarma yapılandırmasını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="78983-109">Update a continuous export configuration in an applciation insights resource</span></span>

## <span data-ttu-id="78983-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="78983-110">EXAMPLES</span></span>

### <span data-ttu-id="78983-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="78983-111">Example 1</span></span>
```
PS C:\> $sastoken = New-AzureStorageContainerSASToken -Name testcontainer -Context $context -ExpiryTime (Get-Date).AddYears(50) -Permission w
PS C:\> $sasuri = "https://teststorageaccount.blob.core.windows.net/testcontainer" + $sastoken
PS C:\> Set-AzureRmApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test"
 -DocumentTypes "Request","Trace" -ExportId "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" -DestinationStorageAccountId "/subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount" -DestinationStorageLocationId sourcecentralus
 -DestinationStorageSASUri $sasuri

ExportId                         : jlTFEiBg1rkDXOCIeJQ2mB2TxZg=
StorageName                      : teststorageaccount
ContainerName                    : testcontainer
DocumentTypes                    : Request, Custom Event, Trace
DestinationStorageSubscriptionId : 50359d91-7b9d-4823-85af-eb298a61ba96
DestinationStorageLocationId     : sourcecentralus
DestinationStorageAccountId      : /subscriptions/50359d91-7b9d-4823-85af-eb298a61ba96/resourceGroups/testgroup/providers/Microsoft.Storage/storageAccounts/teststorageaccount
IsEnabled                        : True
ExportStatus                     : Preparing
LastSuccessTime                  :
```

<span data-ttu-id="78983-112">"Testgroup" kaynak grubundaki "jlTFEiBg1rkDXOCIeJQ2mB2TxZg =" kaynak grubundaki sürekli dışarı aktarma yapılandırmasını "=" kaynak grubunda "teststorageaccount" içinde "testcontainer" depolama kapsayıcısına aktarmak için güncelleştirin. SAS belirtecinin geçerli olması ve kapsayıcıya yazma izni olması gerekir, aksi takdirde dışarı aktarma özelliği çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="78983-112">Update continuous export configuration "jlTFEiBg1rkDXOCIeJQ2mB2TxZg=" of resource "test" in resource group "testgroup" to export "Request" and "Trace" documents to storage container "testcontainer" in "teststorageaccount".The SAS token have to be valid and have write permission to the container, otherwise continous export feature won't work.</span></span> <span data-ttu-id="78983-113">SAS belirtecinin süresi dolduysa, sürekli dışarı aktarma özelliği çalışmayı durdurur.</span><span class="sxs-lookup"><span data-stu-id="78983-113">If SAS token expired, the continuous export feature will stop working.</span></span>

## <span data-ttu-id="78983-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="78983-114">PARAMETERS</span></span>

### <span data-ttu-id="78983-115">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="78983-115">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="78983-116">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="78983-116">Application Insights Component Object.</span></span>

```yaml
Type: PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="78983-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="78983-117">-Confirm</span></span>
<span data-ttu-id="78983-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="78983-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78983-119">-DefaultProfile</span></span>
<span data-ttu-id="78983-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="78983-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-121">-DisableConfiguration</span><span class="sxs-lookup"><span data-stu-id="78983-121">-DisableConfiguration</span></span>
<span data-ttu-id="78983-122">Sürekli dışarı aktarmayı devre dışı bırakın.</span><span class="sxs-lookup"><span data-stu-id="78983-122">Disable continuous export or not.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-123">-DocumentType</span><span class="sxs-lookup"><span data-stu-id="78983-123">-DocumentType</span></span>
<span data-ttu-id="78983-124">Dışarı aktarılan belge türleri.</span><span class="sxs-lookup"><span data-stu-id="78983-124">Document types that need exported.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Request, Exception, Custom Event, Trace, Metric, Page Load, Page View, Dependency, Availability, Performance Counter

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-125">-ExportId</span><span class="sxs-lookup"><span data-stu-id="78983-125">-ExportId</span></span>
<span data-ttu-id="78983-126">Application Insights sürekli dışarı aktarma kimliği.</span><span class="sxs-lookup"><span data-stu-id="78983-126">Application Insights Continuous Export Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-127">-Ad</span><span class="sxs-lookup"><span data-stu-id="78983-127">-Name</span></span>
<span data-ttu-id="78983-128">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="78983-128">Application Insights Component Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78983-129">-ResourceGroupName</span></span>
<span data-ttu-id="78983-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="78983-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ComponentNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="78983-131">-ResourceId</span></span>
<span data-ttu-id="78983-132">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="78983-132">Application Insights Component Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="78983-133">-Storageaccountıd</span><span class="sxs-lookup"><span data-stu-id="78983-133">-StorageAccountId</span></span>
<span data-ttu-id="78983-134">Hedef depolama hesap kimliği.</span><span class="sxs-lookup"><span data-stu-id="78983-134">Destination Storage Account Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-135">-StorageLocation</span><span class="sxs-lookup"><span data-stu-id="78983-135">-StorageLocation</span></span>
<span data-ttu-id="78983-136">Hedef depolama konumu kimliği.</span><span class="sxs-lookup"><span data-stu-id="78983-136">Destination Storage Location Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-137">-StorageSASUri</span><span class="sxs-lookup"><span data-stu-id="78983-137">-StorageSASUri</span></span>
<span data-ttu-id="78983-138">Hedef depolama SAS Uri 'si.</span><span class="sxs-lookup"><span data-stu-id="78983-138">Destination Storage SAS uri.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78983-139">-WhatIf</span></span>
<span data-ttu-id="78983-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="78983-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="78983-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="78983-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78983-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78983-142">CommonParameters</span></span>
<span data-ttu-id="78983-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="78983-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78983-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78983-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78983-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="78983-145">INPUTS</span></span>

### <span data-ttu-id="78983-146">System. String</span><span class="sxs-lookup"><span data-stu-id="78983-146">System.String</span></span>
<span data-ttu-id="78983-147">System. String [] System. Boolean</span><span class="sxs-lookup"><span data-stu-id="78983-147">System.String[] System.Boolean</span></span>

## <span data-ttu-id="78983-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="78983-148">OUTPUTS</span></span>

### <span data-ttu-id="78983-149">Microsoft. Azure. Commands. ApplicationInsights. model. PSExportConfiguration</span><span class="sxs-lookup"><span data-stu-id="78983-149">Microsoft.Azure.Commands.ApplicationInsights.Models.PSExportConfiguration</span></span>

## <span data-ttu-id="78983-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="78983-150">NOTES</span></span>

## <span data-ttu-id="78983-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="78983-151">RELATED LINKS</span></span>

