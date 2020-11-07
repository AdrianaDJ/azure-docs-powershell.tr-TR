---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroupmember
schema: 2.0.0
ms.openlocfilehash: 3b1af5134147ad099547d95fdf5dbf79850e464a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938767"
---
# <span data-ttu-id="754c4-101">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="754c4-101">Remove-AzureRmADGroupMember</span></span>

## <span data-ttu-id="754c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="754c4-102">SYNOPSIS</span></span>
<span data-ttu-id="754c4-103">Bir AD grubundan kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="754c4-103">Removes a user from an AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="754c4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="754c4-104">SYNTAX</span></span>

### <span data-ttu-id="754c4-105">Açıkça Itparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="754c4-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzureRmADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="754c4-106">Memberobjectivseçwithgroupdisplayname</span><span class="sxs-lookup"><span data-stu-id="754c4-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754c4-107">Memberobjectivseçwithbject</span><span class="sxs-lookup"><span data-stu-id="754c4-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754c4-108">Memberobjectivseçwithgroupobjectid</span><span class="sxs-lookup"><span data-stu-id="754c4-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754c4-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="754c4-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754c4-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="754c4-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="754c4-111">Memberupnwithgroupobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="754c4-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="754c4-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="754c4-112">DESCRIPTION</span></span>
<span data-ttu-id="754c4-113">Bir AD grubundan kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="754c4-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="754c4-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="754c4-114">EXAMPLES</span></span>

### <span data-ttu-id="754c4-115">Örnek 1-Group By nesne kimliğinden Kullanıcı kaldırma</span><span class="sxs-lookup"><span data-stu-id="754c4-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="754c4-116">Nesne kimliği ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' olan kullanıcıyı nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan gruptan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="754c4-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="754c4-117">Örnek 2-şeridi kullanarak gruptan bir kullanıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="754c4-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="754c4-118">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve Remove-AzureRmADGroupMember yöneltmeleri</span><span class="sxs-lookup"><span data-stu-id="754c4-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzureRmADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="754c4-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="754c4-119">PARAMETERS</span></span>

### <span data-ttu-id="754c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="754c4-120">-DefaultProfile</span></span>
<span data-ttu-id="754c4-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="754c4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="754c4-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="754c4-122">-GroupDisplayName</span></span>
<span data-ttu-id="754c4-123">Üyeleri kaldırılacak grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="754c4-123">The display name of the group to remove the member(s) from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754c4-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="754c4-124">-GroupObject</span></span>
<span data-ttu-id="754c4-125">Üyenin kaldırılacağı grubun nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="754c4-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="754c4-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="754c4-126">-GroupObjectId</span></span>
<span data-ttu-id="754c4-127">Üyenin kaldırılacağı grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="754c4-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754c4-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="754c4-128">-MemberObjectId</span></span>
<span data-ttu-id="754c4-129">Üyenin nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="754c4-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754c4-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="754c4-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="754c4-131">Kaldırılacak üyelerin UPN 'si.</span><span class="sxs-lookup"><span data-stu-id="754c4-131">The UPN of the member(s) to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="754c4-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="754c4-132">-PassThru</span></span>
<span data-ttu-id="754c4-133">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="754c4-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="754c4-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="754c4-134">-Confirm</span></span>
<span data-ttu-id="754c4-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="754c4-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="754c4-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="754c4-136">-WhatIf</span></span>
<span data-ttu-id="754c4-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="754c4-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="754c4-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="754c4-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="754c4-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="754c4-139">CommonParameters</span></span>
<span data-ttu-id="754c4-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="754c4-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="754c4-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="754c4-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="754c4-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="754c4-142">INPUTS</span></span>

### <span data-ttu-id="754c4-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="754c4-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="754c4-144">Parametreler: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="754c4-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="754c4-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="754c4-145">OUTPUTS</span></span>

### <span data-ttu-id="754c4-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="754c4-146">System.Boolean</span></span>

## <span data-ttu-id="754c4-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="754c4-147">NOTES</span></span>

## <span data-ttu-id="754c4-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="754c4-148">RELATED LINKS</span></span>
