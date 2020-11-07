---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 9c860726993929a6618706037b5c53dff14a68ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763629"
---
# <span data-ttu-id="e9719-101">New-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="e9719-101">New-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="e9719-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9719-102">SYNOPSIS</span></span>
<span data-ttu-id="e9719-103">İlke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9719-103">Creates a policy set definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9719-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9719-104">SYNTAX</span></span>

```
New-AzureRmPolicySetDefinition -Name <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyDefinition <String> [-Parameter <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9719-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9719-105">DESCRIPTION</span></span>
<span data-ttu-id="e9719-106">**New-AzureRmPolicySetDefinition** cmdlet 'i bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9719-106">The **New-AzureRmPolicySetDefinition** cmdlet creates a policy set definition.</span></span>

## <span data-ttu-id="e9719-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9719-107">EXAMPLES</span></span>

### <span data-ttu-id="e9719-108">Örnek 1: ilke kümesi dosyası kullanarak ilke kümesi tanımı oluşturma</span><span class="sxs-lookup"><span data-stu-id="e9719-108">Example 1: Create a policy set definition by using a policy set file</span></span>
```
PS C:\>New-AzureRmPolicySetDefinition -Name "VMPolicyDefinition" -PolicyDefinition C:\VMPolicySet.json
```

<span data-ttu-id="e9719-109">Bu komut, C:\VMPolicy.jsüzerinde belirtilen ilke tanımlarını içeren VMPolicyDefinition adlı bir ilke kümesi tanımı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e9719-109">This command creates a policy set definition named VMPolicyDefinition that contains the policy definitions specified in C:\VMPolicy.json.</span></span>

## <span data-ttu-id="e9719-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9719-110">PARAMETERS</span></span>

### <span data-ttu-id="e9719-111">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="e9719-111">-ApiVersion</span></span>
<span data-ttu-id="e9719-112">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9719-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e9719-113">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e9719-113">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9719-114">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="e9719-114">-Description</span></span>
<span data-ttu-id="e9719-115">İlke kümesi tanımının açıklaması.</span><span class="sxs-lookup"><span data-stu-id="e9719-115">The description for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9719-116">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e9719-116">-DisplayName</span></span>
<span data-ttu-id="e9719-117">İlke kümesi tanımının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="e9719-117">The display name for policy set definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9719-118">-Ad</span><span class="sxs-lookup"><span data-stu-id="e9719-118">-Name</span></span>
<span data-ttu-id="e9719-119">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="e9719-119">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9719-120">-Parametre</span><span class="sxs-lookup"><span data-stu-id="e9719-120">-Parameter</span></span>
<span data-ttu-id="e9719-121">İlke kümesi tanımı için parametreler bildirimi.</span><span class="sxs-lookup"><span data-stu-id="e9719-121">The parameters declaration for policy set definition.</span></span>
<span data-ttu-id="e9719-122">Bu, Parameters bildirimini veya Parameters bildirimini içeren bir dosya adına yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="e9719-122">This can either be a path to a file name containing the parameters declaration, or the parameters declaration as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9719-123">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="e9719-123">-PolicyDefinition</span></span>
<span data-ttu-id="e9719-124">İlke kümesi tanımı.</span><span class="sxs-lookup"><span data-stu-id="e9719-124">The policy set definition.</span></span> <span data-ttu-id="e9719-125">Bu, ilke tanımlarını içeren bir dosya adına veya ilke kümesi tanımına dize olarak bir yol olabilir.</span><span class="sxs-lookup"><span data-stu-id="e9719-125">This can either be a path to a file name containing the policy definitions, or the policy set definition as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9719-126">-Pre-</span><span class="sxs-lookup"><span data-stu-id="e9719-126">-Pre</span></span>
<span data-ttu-id="e9719-127">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="e9719-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e9719-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="e9719-128">-Confirm</span></span>
<span data-ttu-id="e9719-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e9719-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9719-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9719-130">-DefaultProfile</span></span>
<span data-ttu-id="e9719-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e9719-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9719-132">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e9719-132">-Metadata</span></span>
<span data-ttu-id="e9719-133">İlke kümesi tanımı için meta veriler.</span><span class="sxs-lookup"><span data-stu-id="e9719-133">The metadata for policy set definition.</span></span> <span data-ttu-id="e9719-134">Bu, meta veri veya meta veri içeren bir dosya adının yolu olabilir.</span><span class="sxs-lookup"><span data-stu-id="e9719-134">This can either be a path to a file name containing the metadata, or the metadata as string.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9719-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9719-135">-WhatIf</span></span>
<span data-ttu-id="e9719-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e9719-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e9719-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e9719-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9719-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9719-138">CommonParameters</span></span>
<span data-ttu-id="e9719-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9719-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9719-140">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9719-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9719-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9719-141">INPUTS</span></span>

### <span data-ttu-id="e9719-142">System. String</span><span class="sxs-lookup"><span data-stu-id="e9719-142">System.String</span></span>

## <span data-ttu-id="e9719-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9719-143">OUTPUTS</span></span>

### <span data-ttu-id="e9719-144">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e9719-144">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e9719-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9719-145">NOTES</span></span>

## <span data-ttu-id="e9719-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9719-146">RELATED LINKS</span></span>

