---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 069705ffc119fae964e931164f97bfbae72eca35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936471"
---
# <span data-ttu-id="2f978-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="2f978-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="2f978-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f978-102">SYNOPSIS</span></span>
<span data-ttu-id="2f978-103">Var olan bir AD grubuna kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="2f978-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="2f978-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2f978-104">SYNTAX</span></span>

### <span data-ttu-id="2f978-105">Memberobjectivseçwithgroupobjectid (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2f978-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f978-106">Memberobjectivseçwithgroupdisplayname</span><span class="sxs-lookup"><span data-stu-id="2f978-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f978-107">Memberobjectivseçwithbject</span><span class="sxs-lookup"><span data-stu-id="2f978-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f978-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f978-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f978-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2f978-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f978-110">Memberupnwithgroupobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="2f978-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f978-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="2f978-111">DESCRIPTION</span></span>
<span data-ttu-id="2f978-112">Var olan bir AD grubuna kullanıcı ekler.</span><span class="sxs-lookup"><span data-stu-id="2f978-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="2f978-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2f978-113">EXAMPLES</span></span>

### <span data-ttu-id="2f978-114">Örnek 1-gruba göre kullanıcıya ekleme kimliği</span><span class="sxs-lookup"><span data-stu-id="2f978-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="2f978-115">Nesne kimliği ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' olan kullanıcıyı nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan gruba ekler.</span><span class="sxs-lookup"><span data-stu-id="2f978-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="2f978-116">Örnek 2-boru by bir gruba kullanıcı ekleme</span><span class="sxs-lookup"><span data-stu-id="2f978-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="2f978-117">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve yöneltmeleri, kullanıcıyı o gruba eklemek için Add-AzADGroupMember cmdlet 'e alır.</span><span class="sxs-lookup"><span data-stu-id="2f978-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="2f978-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2f978-118">PARAMETERS</span></span>

### <span data-ttu-id="2f978-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f978-119">-DefaultProfile</span></span>
<span data-ttu-id="2f978-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2f978-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f978-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="2f978-121">-MemberObjectId</span></span>
<span data-ttu-id="2f978-122">Üyenin nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="2f978-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f978-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="2f978-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="2f978-124">Gruba eklenecek üyelerin UPN 'si.</span><span class="sxs-lookup"><span data-stu-id="2f978-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="2f978-125">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2f978-125">-PassThru</span></span>
<span data-ttu-id="2f978-126">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="2f978-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="2f978-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="2f978-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="2f978-128">Üyelerin ekleneceği grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="2f978-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="2f978-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="2f978-129">-TargetGroupObject</span></span>
<span data-ttu-id="2f978-130">Üyelerin ekleneceği grubun nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="2f978-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="2f978-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="2f978-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="2f978-132">Üyelerin ekleneceği grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="2f978-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="2f978-133">-Onay</span><span class="sxs-lookup"><span data-stu-id="2f978-133">-Confirm</span></span>
<span data-ttu-id="2f978-134">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2f978-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f978-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f978-135">-WhatIf</span></span>
<span data-ttu-id="2f978-136">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2f978-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f978-137">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2f978-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f978-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f978-138">CommonParameters</span></span>
<span data-ttu-id="2f978-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2f978-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f978-140">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f978-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f978-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2f978-141">INPUTS</span></span>

### <span data-ttu-id="2f978-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="2f978-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="2f978-143">Parametreler: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2f978-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="2f978-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2f978-144">OUTPUTS</span></span>

### <span data-ttu-id="2f978-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2f978-145">System.Boolean</span></span>

## <span data-ttu-id="2f978-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2f978-146">NOTES</span></span>

## <span data-ttu-id="2f978-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2f978-147">RELATED LINKS</span></span>
