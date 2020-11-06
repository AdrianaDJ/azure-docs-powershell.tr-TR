---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicysetdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: ea36cf36b32df4c61c159e89cfdae12acdcc9509
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591622"
---
# <span data-ttu-id="934a1-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="934a1-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="934a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="934a1-102">SYNOPSIS</span></span>
<span data-ttu-id="934a1-103">İlke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="934a1-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="934a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="934a1-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="934a1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="934a1-105">DESCRIPTION</span></span>
<span data-ttu-id="934a1-106">**New-AzureRmPolicySetDefinition** cmdlet 'i bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="934a1-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="934a1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="934a1-107">EXAMPLES</span></span>

### <span data-ttu-id="934a1-108">Örnek 1: ilke kümesi dosyası kullanarak ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="934a1-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="934a1-109">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke tanımlarını içeren VMPolicyDefinition adlı bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="934a1-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="934a1-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="934a1-110">PARAMETERS</span></span>

### <span data-ttu-id="934a1-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="934a1-111">-ApiVersion</span></span>
<span data-ttu-id="934a1-112">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="934a1-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="934a1-113">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="934a1-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="934a1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="934a1-114">-DefaultProfile</span></span>
<span data-ttu-id="934a1-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="934a1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="934a1-116">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="934a1-116">-Description</span></span>
<span data-ttu-id="934a1-117">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="934a1-117">The description for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934a1-118">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="934a1-118">-DisplayName</span></span>
<span data-ttu-id="934a1-119">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="934a1-119">The display name for policy set definition.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934a1-120">-Metadata</span><span class="sxs-lookup"><span data-stu-id="934a1-120">-Metadata</span></span>
<span data-ttu-id="934a1-121">İlke kümesi tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="934a1-121">The metadata for policy set definition.</span></span> <span data-ttu-id="934a1-122">Bu, meta veri içeren bir dosya adının yolu veya dize olarak meta veri olabilir</span><span class="sxs-lookup"><span data-stu-id="934a1-122">This can either be a path to a file name containing the metadata, or the metadata as string</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934a1-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="934a1-123">-Name</span></span>
<span data-ttu-id="934a1-124">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="934a1-124">The policy set definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934a1-125">-Parametre</span><span class="sxs-lookup"><span data-stu-id="934a1-125">-Parameter</span></span>
<span data-ttu-id="934a1-126">İlke kümesi tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="934a1-126">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="934a1-127">Bu, Parameters bildirimini veya Parameters bildirimini içeren bir dosya adına yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="934a1-127">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934a1-128">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="934a1-128">-PolicyDefinition</span></span>
<span data-ttu-id="934a1-129">İlke kümesi tanımı.</span><span class="sxs-lookup"><span data-stu-id="934a1-129">The policy set definition.</span></span> <span data-ttu-id="934a1-130">Bu, ilke tanımlarını içeren bir dosya adına veya ilke kümesi tanımına dize olarak bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="934a1-130">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="934a1-131">-Pre-</span><span class="sxs-lookup"><span data-stu-id="934a1-131">-Pre</span></span>
<span data-ttu-id="934a1-132">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="934a1-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="934a1-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="934a1-133">-Confirm</span></span>
<span data-ttu-id="934a1-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="934a1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="934a1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="934a1-135">-WhatIf</span></span>
<span data-ttu-id="934a1-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="934a1-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="934a1-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="934a1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="934a1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="934a1-138">CommonParameters</span></span>
<span data-ttu-id="934a1-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="934a1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="934a1-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="934a1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="934a1-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="934a1-141">INPUTS</span></span>

### <span data-ttu-id="934a1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="934a1-142">System.String</span></span>

## <span data-ttu-id="934a1-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="934a1-143">OUTPUTS</span></span>

### <span data-ttu-id="934a1-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="934a1-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="934a1-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="934a1-145">NOTES</span></span>

## <span data-ttu-id="934a1-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="934a1-146">RELATED LINKS</span></span>
