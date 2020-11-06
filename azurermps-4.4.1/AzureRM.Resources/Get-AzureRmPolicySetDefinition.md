---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmPolicySetDefinition.md
ms.openlocfilehash: 5fba45e50076952a0a2e11e2e5541ab9546d3bc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592586"
---
# <span data-ttu-id="980a3-101">Get-AzureRmPolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="980a3-101">Get-AzureRmPolicySetDefinition</span></span>

## <span data-ttu-id="980a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="980a3-102">SYNOPSIS</span></span>
<span data-ttu-id="980a3-103">İlke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="980a3-103">Gets policy set definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="980a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="980a3-104">SYNTAX</span></span>

### <span data-ttu-id="980a3-105">Tüm ilke kümesi tanımları parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="980a3-105">The list all policy set definitions parameter set.</span></span> <span data-ttu-id="980a3-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="980a3-106">(Default)</span></span>
```
Get-AzureRmPolicySetDefinition [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="980a3-107">İlke kümesi tanım adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="980a3-107">The policy set definition name parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Name <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="980a3-108">İlke kümesi tanım kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="980a3-108">The policy set definition Id parameter set.</span></span>
```
Get-AzureRmPolicySetDefinition -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="980a3-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="980a3-109">DESCRIPTION</span></span>
<span data-ttu-id="980a3-110">**Get-AzureRmPolicySetDefinition** cmdlet 'i, tüm ilke kümesi tanımlarını veya ad veya kimlikle tanımlanan belirli bir ilke kümesi tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="980a3-110">The **Get-AzureRmPolicySetDefinition** cmdlet gets all the policy set definitions or a specific policy set definition identified by name or ID.</span></span>

## <span data-ttu-id="980a3-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="980a3-111">EXAMPLES</span></span>

### <span data-ttu-id="980a3-112">Örnek 1: tüm ilke kümesi tanımını alma</span><span class="sxs-lookup"><span data-stu-id="980a3-112">Example 1: Get all policy set definition</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition
```

<span data-ttu-id="980a3-113">Bu komut, tüm ilke kümesi tanımlarını alır.</span><span class="sxs-lookup"><span data-stu-id="980a3-113">This command gets all the policy set definitions.</span></span>

### <span data-ttu-id="980a3-114">Örnek 2: ada göre ilke kümesi tanımını alma</span><span class="sxs-lookup"><span data-stu-id="980a3-114">Example 2: Get policy set definition by name</span></span>
```
PS C:\>Get-AzureRmPolicySetDefinition -Name "VMPolicyDefinition"
```

<span data-ttu-id="980a3-115">Bu komut, VMPolicyDefinition adındaki ilke kümesi tanımını alır.</span><span class="sxs-lookup"><span data-stu-id="980a3-115">This command gets the policy set definition named VMPolicyDefinition.</span></span>

## <span data-ttu-id="980a3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="980a3-116">PARAMETERS</span></span>

### <span data-ttu-id="980a3-117">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="980a3-117">-ApiVersion</span></span>
<span data-ttu-id="980a3-118">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="980a3-118">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="980a3-119">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="980a3-119">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="980a3-120">-ID</span><span class="sxs-lookup"><span data-stu-id="980a3-120">-Id</span></span>
<span data-ttu-id="980a3-121">Abonelik dahil tam nitelikli ilke kümesi tanım kimliği.</span><span class="sxs-lookup"><span data-stu-id="980a3-121">The fully qualified policy set definition Id, including the subscription.</span></span>
<span data-ttu-id="980a3-122">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="980a3-122">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="980a3-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="980a3-123">-Name</span></span>
<span data-ttu-id="980a3-124">İlke kümesi tanım adı.</span><span class="sxs-lookup"><span data-stu-id="980a3-124">The policy set definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The policy set definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="980a3-125">-Pre-</span><span class="sxs-lookup"><span data-stu-id="980a3-125">-Pre</span></span>
<span data-ttu-id="980a3-126">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="980a3-126">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="980a3-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="980a3-127">-DefaultProfile</span></span>
<span data-ttu-id="980a3-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="980a3-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="980a3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="980a3-129">CommonParameters</span></span>
<span data-ttu-id="980a3-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="980a3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="980a3-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="980a3-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="980a3-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="980a3-132">INPUTS</span></span>

### <span data-ttu-id="980a3-133">System. String</span><span class="sxs-lookup"><span data-stu-id="980a3-133">System.String</span></span>

## <span data-ttu-id="980a3-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="980a3-134">OUTPUTS</span></span>

### <span data-ttu-id="980a3-135">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="980a3-135">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="980a3-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="980a3-136">NOTES</span></span>

## <span data-ttu-id="980a3-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="980a3-137">RELATED LINKS</span></span>

