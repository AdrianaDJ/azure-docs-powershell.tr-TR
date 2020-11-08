---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 5424c2b6332455c0b0cfa04526295d9e51f46fdc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095877"
---
# <span data-ttu-id="785cc-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="785cc-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="785cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="785cc-102">SYNOPSIS</span></span>
<span data-ttu-id="785cc-103">Var olan bir AD grubuna kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="785cc-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="785cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="785cc-104">SYNTAX</span></span>

### <span data-ttu-id="785cc-105">Memberobjectivseçwithgroupobjectid (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="785cc-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cc-106">Memberobjectivseçwithgroupdisplayname</span><span class="sxs-lookup"><span data-stu-id="785cc-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cc-107">Memberobjectivseçwithbject</span><span class="sxs-lookup"><span data-stu-id="785cc-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cc-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cc-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cc-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="785cc-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="785cc-110">Memberupnwithgroupobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="785cc-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="785cc-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="785cc-111">DESCRIPTION</span></span>
<span data-ttu-id="785cc-112">Var olan bir AD grubuna kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="785cc-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="785cc-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="785cc-113">EXAMPLES</span></span>

### <span data-ttu-id="785cc-114">Örnek 1-gruba göre kullanıcıya ekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="785cc-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="785cc-115">Nesne kimliği ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' olan kullanıcıyı nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan gruba ekler.</span><span class="sxs-lookup"><span data-stu-id="785cc-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="785cc-116">Örnek 2-boru by bir gruba kullanıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="785cc-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="785cc-117">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve yöneltmeleri, kullanıcıyı o gruba eklemek için Add-AzADGroupMember cmdlet 'e alır.</span><span class="sxs-lookup"><span data-stu-id="785cc-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="785cc-118">Örnek 3-gruba göre bir kullanıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="785cc-118">Example 3 - Add a user to a group by principal name</span></span>

```
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="785cc-119">Gruba bir kullanıcı ekler ve grubun üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="785cc-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="785cc-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="785cc-120">PARAMETERS</span></span>

### <span data-ttu-id="785cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785cc-121">-DefaultProfile</span></span>
<span data-ttu-id="785cc-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="785cc-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="785cc-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="785cc-123">-MemberObjectId</span></span>
<span data-ttu-id="785cc-124">Üyenin nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="785cc-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785cc-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="785cc-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="785cc-126">Gruba eklenecek üyelerin UPN 'si.</span><span class="sxs-lookup"><span data-stu-id="785cc-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="785cc-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="785cc-127">-PassThru</span></span>
<span data-ttu-id="785cc-128">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="785cc-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="785cc-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="785cc-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="785cc-130">Üyelerin ekleneceği grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="785cc-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="785cc-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="785cc-131">-TargetGroupObject</span></span>
<span data-ttu-id="785cc-132">Üyelerin ekleneceği grubun nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="785cc-132">The object representation of the group to add the member(s) to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="785cc-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="785cc-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="785cc-134">Üyelerin ekleneceği grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="785cc-134">The object id of the group to add the member(s) to.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="785cc-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="785cc-135">-Confirm</span></span>
<span data-ttu-id="785cc-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="785cc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="785cc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="785cc-137">-WhatIf</span></span>
<span data-ttu-id="785cc-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="785cc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="785cc-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="785cc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="785cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785cc-140">CommonParameters</span></span>
<span data-ttu-id="785cc-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="785cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785cc-142">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="785cc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785cc-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="785cc-143">INPUTS</span></span>

### <span data-ttu-id="785cc-144">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="785cc-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="785cc-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="785cc-145">OUTPUTS</span></span>

### <span data-ttu-id="785cc-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="785cc-146">System.Boolean</span></span>

## <span data-ttu-id="785cc-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="785cc-147">NOTES</span></span>

## <span data-ttu-id="785cc-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="785cc-148">RELATED LINKS</span></span>
