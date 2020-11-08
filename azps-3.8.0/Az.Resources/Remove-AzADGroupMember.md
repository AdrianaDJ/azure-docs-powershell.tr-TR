---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 23fa2a476c831216c93796e52267da68debab971
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096279"
---
# <span data-ttu-id="c265e-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="c265e-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="c265e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c265e-102">SYNOPSIS</span></span>
<span data-ttu-id="c265e-103">Bir AD grubundan kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c265e-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="c265e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c265e-104">SYNTAX</span></span>

### <span data-ttu-id="c265e-105">Açıkça Itparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c265e-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c265e-106">Memberobjectivseçwithgroupdisplayname</span><span class="sxs-lookup"><span data-stu-id="c265e-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c265e-107">Memberobjectivseçwithbject</span><span class="sxs-lookup"><span data-stu-id="c265e-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c265e-108">Memberobjectivseçwithgroupobjectid</span><span class="sxs-lookup"><span data-stu-id="c265e-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c265e-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c265e-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c265e-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c265e-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c265e-111">Memberupnwithgroupobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c265e-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c265e-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="c265e-112">DESCRIPTION</span></span>
<span data-ttu-id="c265e-113">Bir AD grubundan kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c265e-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="c265e-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c265e-114">EXAMPLES</span></span>

### <span data-ttu-id="c265e-115">Örnek 1-Group By nesne kimliğinden Kullanıcı kaldırma</span><span class="sxs-lookup"><span data-stu-id="c265e-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c265e-116">Nesne kimliği ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' olan kullanıcıyı nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan gruptan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c265e-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="c265e-117">Örnek 2-şeridi kullanarak gruptan bir kullanıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="c265e-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="c265e-118">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve Remove-AzADGroupMember yöneltmeleri</span><span class="sxs-lookup"><span data-stu-id="c265e-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="c265e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c265e-119">PARAMETERS</span></span>

### <span data-ttu-id="c265e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c265e-120">-DefaultProfile</span></span>
<span data-ttu-id="c265e-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c265e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c265e-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="c265e-122">-GroupDisplayName</span></span>
<span data-ttu-id="c265e-123">Üyeleri kaldırılacak grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="c265e-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="c265e-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="c265e-124">-GroupObject</span></span>
<span data-ttu-id="c265e-125">Üyenin kaldırılacağı grubun nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="c265e-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="c265e-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="c265e-126">-GroupObjectId</span></span>
<span data-ttu-id="c265e-127">Üyenin kaldırılacağı grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="c265e-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="c265e-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="c265e-128">-MemberObjectId</span></span>
<span data-ttu-id="c265e-129">Üyenin nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="c265e-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c265e-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c265e-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="c265e-131">Kaldırılacak üyelerin UPN 'si.</span><span class="sxs-lookup"><span data-stu-id="c265e-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="c265e-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="c265e-132">-PassThru</span></span>
<span data-ttu-id="c265e-133">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="c265e-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c265e-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="c265e-134">-Confirm</span></span>
<span data-ttu-id="c265e-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c265e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c265e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c265e-136">-WhatIf</span></span>
<span data-ttu-id="c265e-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c265e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c265e-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c265e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c265e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c265e-139">CommonParameters</span></span>
<span data-ttu-id="c265e-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c265e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c265e-141">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c265e-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c265e-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c265e-142">INPUTS</span></span>

### <span data-ttu-id="c265e-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="c265e-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="c265e-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c265e-144">OUTPUTS</span></span>

### <span data-ttu-id="c265e-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c265e-145">System.Boolean</span></span>

## <span data-ttu-id="c265e-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c265e-146">NOTES</span></span>

## <span data-ttu-id="c265e-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c265e-147">RELATED LINKS</span></span>
