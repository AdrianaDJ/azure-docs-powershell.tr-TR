---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589843"
---
# <span data-ttu-id="38e5f-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38e5f-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="38e5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38e5f-102">SYNOPSIS</span></span>
<span data-ttu-id="38e5f-103">Tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38e5f-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38e5f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38e5f-104">SYNTAX</span></span>

### <span data-ttu-id="38e5f-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38e5f-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38e5f-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="38e5f-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e5f-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="38e5f-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38e5f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="38e5f-108">DESCRIPTION</span></span>
<span data-ttu-id="38e5f-109">Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet 'i belirli parametrelerle tümleştirme çalışma zamanını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38e5f-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="38e5f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38e5f-110">EXAMPLES</span></span>

### <span data-ttu-id="38e5f-111">Örnek 1: güncelleştirme tümleştirmesi çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="38e5f-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="38e5f-112">Cmdlet, ' test-Selfhost-IR ' adlı tümleştirme çalışma zamanının açıklamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="38e5f-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="38e5f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38e5f-113">PARAMETERS</span></span>

### <span data-ttu-id="38e5f-114">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="38e5f-114">-AuthKey</span></span>
<span data-ttu-id="38e5f-115">Self-hosted Integration Runtime 'ın kimlik doğrulama anahtarı.</span><span class="sxs-lookup"><span data-stu-id="38e5f-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="38e5f-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="38e5f-117">Tümleştirme çalışma zamanının Katalog veritabanı yöneticisi kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="38e5f-117">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="38e5f-118">-CatalogPricingTier</span></span>
<span data-ttu-id="38e5f-119">Tümleştirme çalışma zamanının Katalog veritabanı fiyatlandırma katmanı.</span><span class="sxs-lookup"><span data-stu-id="38e5f-119">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="38e5f-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="38e5f-121">Tümleştirme çalışma zamanının Katalog veritabanı sunucusu uç noktası.</span><span class="sxs-lookup"><span data-stu-id="38e5f-121">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-122">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="38e5f-122">-DataFactoryName</span></span>
<span data-ttu-id="38e5f-123">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="38e5f-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e5f-124">-DefaultProfile</span></span>
<span data-ttu-id="38e5f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="38e5f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38e5f-126">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="38e5f-126">-Description</span></span>
<span data-ttu-id="38e5f-127">Tümleştirme çalışma zamanı açıklaması.</span><span class="sxs-lookup"><span data-stu-id="38e5f-127">The integration runtime description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-128">-Edition</span><span class="sxs-lookup"><span data-stu-id="38e5f-128">-Edition</span></span>
<span data-ttu-id="38e5f-129">Standart veya kurumsal olabilecek SSIS tümleştirmesi çalışma zamanı modülü, belirtilmemişse varsayılan standart olur.</span><span class="sxs-lookup"><span data-stu-id="38e5f-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="38e5f-130">-Force</span></span>
<span data-ttu-id="38e5f-131">Onay istemeden cmdlet 'i çalıştırır.</span><span class="sxs-lookup"><span data-stu-id="38e5f-131">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="38e5f-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38e5f-132">-InputObject</span></span>
<span data-ttu-id="38e5f-133">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="38e5f-133">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="38e5f-134">-LicenseType</span></span>
<span data-ttu-id="38e5f-135">SıR için seçmek istediğiniz lisans türü.</span><span class="sxs-lookup"><span data-stu-id="38e5f-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="38e5f-136">İki tür vardır: Licenseeklenmiş veya temel fiyat.</span><span class="sxs-lookup"><span data-stu-id="38e5f-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="38e5f-137">Azure Karma Kullanım Avantajı (AHUB) fiyatlandırması yeterliği Kazanmıyorsanız, lütfen temel fiyat seçeneğini belirleyin.</span><span class="sxs-lookup"><span data-stu-id="38e5f-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="38e5f-138">Yoksa, lütfen License'i seçin.</span><span class="sxs-lookup"><span data-stu-id="38e5f-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-139">-Konum</span><span class="sxs-lookup"><span data-stu-id="38e5f-139">-Location</span></span>
<span data-ttu-id="38e5f-140">Tümleştirme çalışma zamanı konumu.</span><span class="sxs-lookup"><span data-stu-id="38e5f-140">The integration runtime location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-141">-Maxparalellexecutionspernode</span><span class="sxs-lookup"><span data-stu-id="38e5f-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="38e5f-142">Yönetilen adanmış tümleştirme çalışma zamanının düğüm başına en yüksek paralel yürütme sayısı.</span><span class="sxs-lookup"><span data-stu-id="38e5f-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-143">-Ad</span><span class="sxs-lookup"><span data-stu-id="38e5f-143">-Name</span></span>
<span data-ttu-id="38e5f-144">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="38e5f-144">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="38e5f-145">-NodeCount</span></span>
<span data-ttu-id="38e5f-146">Tümleştirme çalışma zamanının hedef düğümler sayısı.</span><span class="sxs-lookup"><span data-stu-id="38e5f-146">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-147">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="38e5f-147">-NodeSize</span></span>
<span data-ttu-id="38e5f-148">Tümleştirme çalışma zamanı düğümü boyutu.</span><span class="sxs-lookup"><span data-stu-id="38e5f-148">The integration runtime node size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38e5f-149">-ResourceGroupName</span></span>
<span data-ttu-id="38e5f-150">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="38e5f-150">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-151">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="38e5f-151">-ResourceId</span></span>
<span data-ttu-id="38e5f-152">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="38e5f-152">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="38e5f-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="38e5f-154">Özel kurulum betiğini içeren Azure Blob kapsayıcısının SAS URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="38e5f-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-155">-Alt ağ</span><span class="sxs-lookup"><span data-stu-id="38e5f-155">-Subnet</span></span>
<span data-ttu-id="38e5f-156">VNet içindeki alt ağın adı.</span><span class="sxs-lookup"><span data-stu-id="38e5f-156">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-157">-Tür</span><span class="sxs-lookup"><span data-stu-id="38e5f-157">-Type</span></span>
<span data-ttu-id="38e5f-158">Tümleştirme çalışma zamanı türü.</span><span class="sxs-lookup"><span data-stu-id="38e5f-158">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="38e5f-159">-VNetId</span></span>
<span data-ttu-id="38e5f-160">Tümleştirme çalışma zamanının birleşen VNet KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="38e5f-160">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38e5f-161">-Onay</span><span class="sxs-lookup"><span data-stu-id="38e5f-161">-Confirm</span></span>
<span data-ttu-id="38e5f-162">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="38e5f-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38e5f-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38e5f-163">-WhatIf</span></span>
<span data-ttu-id="38e5f-164">Cmdlet çalışırsa ne olacağını gösterir, ancak cmdlet 'i çalıştırmaz.</span><span class="sxs-lookup"><span data-stu-id="38e5f-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="38e5f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e5f-165">CommonParameters</span></span>
<span data-ttu-id="38e5f-166">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38e5f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e5f-167">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38e5f-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e5f-168">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38e5f-168">INPUTS</span></span>

### <span data-ttu-id="38e5f-169">System. String</span><span class="sxs-lookup"><span data-stu-id="38e5f-169">System.String</span></span>
<span data-ttu-id="38e5f-170">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="38e5f-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="38e5f-171">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38e5f-171">OUTPUTS</span></span>

### <span data-ttu-id="38e5f-172">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="38e5f-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="38e5f-173">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38e5f-173">NOTES</span></span>

## <span data-ttu-id="38e5f-174">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38e5f-174">RELATED LINKS</span></span>

[<span data-ttu-id="38e5f-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="38e5f-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
