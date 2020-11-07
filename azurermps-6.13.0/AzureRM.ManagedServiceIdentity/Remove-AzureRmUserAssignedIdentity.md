---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 03d73ac28bc1869452ecc96b5c867fcbb8c372c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764359"
---
# <span data-ttu-id="327e2-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="327e2-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="327e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="327e2-102">SYNOPSIS</span></span>
<span data-ttu-id="327e2-103">Kullanıcının atadığı kimliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="327e2-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="327e2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="327e2-104">SYNTAX</span></span>

### <span data-ttu-id="327e2-105">ResourceGroupAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="327e2-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="327e2-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="327e2-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="327e2-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="327e2-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="327e2-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="327e2-108">DESCRIPTION</span></span>
<span data-ttu-id="327e2-109">**Remove-Azurermuseratandidentity** belirtilen kullanıcının atadığı kimliği siler.</span><span class="sxs-lookup"><span data-stu-id="327e2-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="327e2-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="327e2-110">EXAMPLES</span></span>

### <span data-ttu-id="327e2-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="327e2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="327e2-112">Bu örnek cmdlet 'i, **ID1** **PSRG**</span><span class="sxs-lookup"><span data-stu-id="327e2-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="327e2-113">Değeri</span><span class="sxs-lookup"><span data-stu-id="327e2-113">True</span></span>

## <span data-ttu-id="327e2-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="327e2-114">PARAMETERS</span></span>

### <span data-ttu-id="327e2-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="327e2-115">-AsJob</span></span>
<span data-ttu-id="327e2-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="327e2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="327e2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327e2-117">-DefaultProfile</span></span>
<span data-ttu-id="327e2-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="327e2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="327e2-119">-Force</span><span class="sxs-lookup"><span data-stu-id="327e2-119">-Force</span></span>
<span data-ttu-id="327e2-120">{{Fill Force açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="327e2-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="327e2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="327e2-121">-InputObject</span></span>
<span data-ttu-id="327e2-122">Identity nesnesi.</span><span class="sxs-lookup"><span data-stu-id="327e2-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="327e2-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="327e2-123">-Name</span></span>
<span data-ttu-id="327e2-124">Kimlik adı.</span><span class="sxs-lookup"><span data-stu-id="327e2-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="327e2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="327e2-125">-ResourceGroupName</span></span>
<span data-ttu-id="327e2-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="327e2-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="327e2-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="327e2-127">-ResourceId</span></span>
<span data-ttu-id="327e2-128">Kimliğin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="327e2-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="327e2-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="327e2-129">-Confirm</span></span>
<span data-ttu-id="327e2-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="327e2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="327e2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="327e2-131">-WhatIf</span></span>
<span data-ttu-id="327e2-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="327e2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="327e2-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="327e2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="327e2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327e2-134">CommonParameters</span></span>
<span data-ttu-id="327e2-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="327e2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327e2-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="327e2-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327e2-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="327e2-137">INPUTS</span></span>

### <span data-ttu-id="327e2-138">Microsoft. Azure. Commands. Managedserviceıdentity. modeller. Psuseratandidentity</span><span class="sxs-lookup"><span data-stu-id="327e2-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>
<span data-ttu-id="327e2-139">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="327e2-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="327e2-140">System. String</span><span class="sxs-lookup"><span data-stu-id="327e2-140">System.String</span></span>

## <span data-ttu-id="327e2-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="327e2-141">OUTPUTS</span></span>

### <span data-ttu-id="327e2-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="327e2-142">System.Boolean</span></span>

## <span data-ttu-id="327e2-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="327e2-143">NOTES</span></span>

## <span data-ttu-id="327e2-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="327e2-144">RELATED LINKS</span></span>
