---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273539"
---
# <span data-ttu-id="4b8c4-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4b8c4-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="4b8c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b8c4-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8c4-103">Kullanıcının atadığı kimliği kaldırır.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="4b8c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4b8c4-104">SYNTAX</span></span>

### <span data-ttu-id="4b8c4-105">ResourceGroupAndNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4b8c4-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8c4-106">Inputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="4b8c4-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b8c4-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="4b8c4-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b8c4-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4b8c4-108">DESCRIPTION</span></span>
<span data-ttu-id="4b8c4-109">**Remove-Azuseratanandentity** belirtilen kullanıcının atadığı kimliği siler.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="4b8c4-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4b8c4-110">EXAMPLES</span></span>

### <span data-ttu-id="4b8c4-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="4b8c4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="4b8c4-112">Bu örnek cmdlet 'i, **ID1** **PSRG**</span><span class="sxs-lookup"><span data-stu-id="4b8c4-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="4b8c4-113">Değeri</span><span class="sxs-lookup"><span data-stu-id="4b8c4-113">True</span></span>

## <span data-ttu-id="4b8c4-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4b8c4-114">PARAMETERS</span></span>

### <span data-ttu-id="4b8c4-115">-Iş</span><span class="sxs-lookup"><span data-stu-id="4b8c4-115">-AsJob</span></span>
<span data-ttu-id="4b8c4-116">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="4b8c4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b8c4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8c4-117">-DefaultProfile</span></span>
<span data-ttu-id="4b8c4-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b8c4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4b8c4-119">-Force</span></span>
<span data-ttu-id="4b8c4-120">{{Fill Force açıklaması}}</span><span class="sxs-lookup"><span data-stu-id="4b8c4-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="4b8c4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b8c4-121">-InputObject</span></span>
<span data-ttu-id="4b8c4-122">Identity nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-122">The Identity object.</span></span>

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

### <span data-ttu-id="4b8c4-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="4b8c4-123">-Name</span></span>
<span data-ttu-id="4b8c4-124">Kimlik adı.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-124">The Identity name.</span></span>

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

### <span data-ttu-id="4b8c4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b8c4-125">-ResourceGroupName</span></span>
<span data-ttu-id="4b8c4-126">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-126">The resource group name.</span></span>

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

### <span data-ttu-id="4b8c4-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4b8c4-127">-ResourceId</span></span>
<span data-ttu-id="4b8c4-128">Kimliğin kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="4b8c4-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="4b8c4-129">-Confirm</span></span>
<span data-ttu-id="4b8c4-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b8c4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b8c4-131">-WhatIf</span></span>
<span data-ttu-id="4b8c4-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b8c4-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b8c4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8c4-134">CommonParameters</span></span>
<span data-ttu-id="4b8c4-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4b8c4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8c4-136">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b8c4-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8c4-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4b8c4-137">INPUTS</span></span>

### <span data-ttu-id="4b8c4-138">Microsoft. Azure. Commands. Managedserviceıdentity. modeller. Psuseratandidentity</span><span class="sxs-lookup"><span data-stu-id="4b8c4-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="4b8c4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4b8c4-139">System.String</span></span>

## <span data-ttu-id="4b8c4-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4b8c4-140">OUTPUTS</span></span>

### <span data-ttu-id="4b8c4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4b8c4-141">System.Boolean</span></span>

## <span data-ttu-id="4b8c4-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4b8c4-142">NOTES</span></span>

## <span data-ttu-id="4b8c4-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4b8c4-143">RELATED LINKS</span></span>
