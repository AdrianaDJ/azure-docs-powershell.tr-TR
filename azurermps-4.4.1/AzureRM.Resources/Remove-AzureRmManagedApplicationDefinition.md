---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmManagedApplicationDefinition.md
ms.openlocfilehash: 2e951452789d57d6d5e126fca80713ef7fd2c584
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593806"
---
# <span data-ttu-id="3e30c-101">Remove-AzureRmManagedApplicationDefinition</span><span class="sxs-lookup"><span data-stu-id="3e30c-101">Remove-AzureRmManagedApplicationDefinition</span></span>

## <span data-ttu-id="3e30c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e30c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e30c-103">Yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="3e30c-103">Removes a managed application definition</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e30c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3e30c-104">SYNTAX</span></span>

### <span data-ttu-id="3e30c-105">Yönetilen uygulama tanımı adı parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="3e30c-105">The managed application definition name parameter set.</span></span> <span data-ttu-id="3e30c-106">Varsayýlan</span><span class="sxs-lookup"><span data-stu-id="3e30c-106">(Default)</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Name <String> -ResourceGroupName <String> [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3e30c-107">Yönetilen uygulama tanımı kimliği parametre kümesi.</span><span class="sxs-lookup"><span data-stu-id="3e30c-107">The managed application definition Id parameter set.</span></span>
```
Remove-AzureRmManagedApplicationDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e30c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="3e30c-108">DESCRIPTION</span></span>
<span data-ttu-id="3e30c-109">**Remove-AzureRmManagedApplicationDefinition** cmdlet 'i yönetilen uygulama tanımını kaldırır</span><span class="sxs-lookup"><span data-stu-id="3e30c-109">The **Remove-AzureRmManagedApplicationDefinition** cmdlet removes a managed application definition</span></span>

## <span data-ttu-id="3e30c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3e30c-110">EXAMPLES</span></span>

### <span data-ttu-id="3e30c-111">Örnek 1: yönetilen uygulama tanımını kaynak KIMLIĞIYLE kaldırma</span><span class="sxs-lookup"><span data-stu-id="3e30c-111">Example 1: Remove managed application definition by resource ID</span></span>
```
PS C:\>$ApplicationDefinition = Get-AzureRmManagedApplicationDefinition -Name "myAppDef" -ResourceGroupName "myRG"
PS C:\>Remove-AzureRmManagedApplicationDefinition -Id $ApplicationDefinition.ResourceId -Force
```

<span data-ttu-id="3e30c-112">İlk komut, Get-AzureRmManagedApplicationDefinition cmdlet 'ini kullanarak myAppDef adlı bir yönetilen uygulama tanımı alır.</span><span class="sxs-lookup"><span data-stu-id="3e30c-112">The first command gets a managed application definition named myAppDef by using the Get-AzureRmManagedApplicationDefinition cmdlet.</span></span>
<span data-ttu-id="3e30c-113">Komut, $ApplicationDefinition değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="3e30c-113">The command stores it in the $ApplicationDefinition variable.</span></span>

<span data-ttu-id="3e30c-114">İkinci komut, $ApplicationDefinition 'in **RESOURCEID** özelliğiyle tanımlanan yönetilen uygulama tanımını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="3e30c-114">The second command removes the managed application definition identified by the **ResourceId** property of $ApplicationDefinition.</span></span>

## <span data-ttu-id="3e30c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3e30c-115">PARAMETERS</span></span>

### <span data-ttu-id="3e30c-116">-Apıversion</span><span class="sxs-lookup"><span data-stu-id="3e30c-116">-ApiVersion</span></span>
<span data-ttu-id="3e30c-117">Ayarlandığında, kullanılacak kaynak sağlayıcısı API sürümünü gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e30c-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3e30c-118">Belirtilmemişse API sürümü otomatik olarak en son kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="3e30c-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3e30c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e30c-119">-DefaultProfile</span></span>
<span data-ttu-id="3e30c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3e30c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e30c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3e30c-121">-Force</span></span>
<span data-ttu-id="3e30c-122">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="3e30c-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3e30c-123">-ID</span><span class="sxs-lookup"><span data-stu-id="3e30c-123">-Id</span></span>
<span data-ttu-id="3e30c-124">Abonelik dahil, tam nitelikli yönetilen uygulama tanımı kimliği.</span><span class="sxs-lookup"><span data-stu-id="3e30c-124">The fully qualified managed application definition Id, including the subscription.</span></span>
<span data-ttu-id="3e30c-125">Örneğin,/Subscriptions/{SubscriptionID}/ResourceGroups/{resourcegroupname}</span><span class="sxs-lookup"><span data-stu-id="3e30c-125">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName}</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition Id parameter set.
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e30c-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="3e30c-126">-Name</span></span>
<span data-ttu-id="3e30c-127">Yönetilen uygulama tanımı adı.</span><span class="sxs-lookup"><span data-stu-id="3e30c-127">The managed application definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e30c-128">-Pre-</span><span class="sxs-lookup"><span data-stu-id="3e30c-128">-Pre</span></span>
<span data-ttu-id="3e30c-129">Ayarlandığında, cmdlet 'in hangi sürümü kullanacağını otomatik olarak belirlerken cmdlet 'in pre API sürümlerini kullanması gerektiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3e30c-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3e30c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e30c-130">-ResourceGroupName</span></span>
<span data-ttu-id="3e30c-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="3e30c-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: The managed application definition name parameter set.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e30c-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="3e30c-132">-Confirm</span></span>
<span data-ttu-id="3e30c-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3e30c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e30c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e30c-134">-WhatIf</span></span>
<span data-ttu-id="3e30c-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3e30c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e30c-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3e30c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e30c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e30c-137">CommonParameters</span></span>
<span data-ttu-id="3e30c-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3e30c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e30c-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e30c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e30c-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3e30c-140">INPUTS</span></span>

### <span data-ttu-id="3e30c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="3e30c-141">System.String</span></span>

## <span data-ttu-id="3e30c-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3e30c-142">OUTPUTS</span></span>

### <span data-ttu-id="3e30c-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3e30c-143">System.Boolean</span></span>

## <span data-ttu-id="3e30c-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3e30c-144">NOTES</span></span>

## <span data-ttu-id="3e30c-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3e30c-145">RELATED LINKS</span></span>

