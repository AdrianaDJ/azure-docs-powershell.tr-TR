---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 1196480735705186ad3493b6c34a473baf35dc0e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933327"
---
# <span data-ttu-id="73aed-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="73aed-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="73aed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73aed-102">SYNOPSIS</span></span>
<span data-ttu-id="73aed-103">Bir AD grubundan kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73aed-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="73aed-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="73aed-104">SYNTAX</span></span>

### <span data-ttu-id="73aed-105">Açıkça Itparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="73aed-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="73aed-106">Memberobjectivseçwithgroupdisplayname</span><span class="sxs-lookup"><span data-stu-id="73aed-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73aed-107">Memberobjectivseçwithbject</span><span class="sxs-lookup"><span data-stu-id="73aed-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73aed-108">Memberobjectivseçwithgroupobjectid</span><span class="sxs-lookup"><span data-stu-id="73aed-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73aed-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="73aed-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73aed-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="73aed-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73aed-111">Memberupnwithgroupobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="73aed-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73aed-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="73aed-112">DESCRIPTION</span></span>
<span data-ttu-id="73aed-113">Bir AD grubundan kullanıcıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73aed-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="73aed-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="73aed-114">EXAMPLES</span></span>

### <span data-ttu-id="73aed-115">Örnek 1-Group By nesne kimliğinden Kullanıcı kaldırma</span><span class="sxs-lookup"><span data-stu-id="73aed-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="73aed-116">Nesne kimliği ' D9076BBC-D62C-4105-9C78-A7F5BC4A3405 ' olan kullanıcıyı nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan gruptan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="73aed-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="73aed-117">Örnek 2-şeridi kullanarak gruptan bir kullanıcıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="73aed-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="73aed-118">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve Remove-AzADGroupMember yöneltmeleri</span><span class="sxs-lookup"><span data-stu-id="73aed-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="73aed-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="73aed-119">PARAMETERS</span></span>

### <span data-ttu-id="73aed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73aed-120">-DefaultProfile</span></span>
<span data-ttu-id="73aed-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="73aed-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73aed-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="73aed-122">-GroupDisplayName</span></span>
<span data-ttu-id="73aed-123">Üyeleri kaldırılacak grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="73aed-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="73aed-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="73aed-124">-GroupObject</span></span>
<span data-ttu-id="73aed-125">Üyenin kaldırılacağı grubun nesne gösterimi.</span><span class="sxs-lookup"><span data-stu-id="73aed-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="73aed-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="73aed-126">-GroupObjectId</span></span>
<span data-ttu-id="73aed-127">Üyenin kaldırılacağı grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="73aed-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="73aed-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="73aed-128">-MemberObjectId</span></span>
<span data-ttu-id="73aed-129">Üyenin nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="73aed-129">The object id of the member.</span></span>

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

### <span data-ttu-id="73aed-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="73aed-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="73aed-131">Kaldırılacak üyelerin UPN 'si.</span><span class="sxs-lookup"><span data-stu-id="73aed-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="73aed-132">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="73aed-132">-PassThru</span></span>
<span data-ttu-id="73aed-133">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="73aed-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="73aed-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="73aed-134">-Confirm</span></span>
<span data-ttu-id="73aed-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="73aed-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73aed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73aed-136">-WhatIf</span></span>
<span data-ttu-id="73aed-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="73aed-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73aed-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="73aed-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73aed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73aed-139">CommonParameters</span></span>
<span data-ttu-id="73aed-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="73aed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73aed-141">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73aed-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73aed-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="73aed-142">INPUTS</span></span>

### <span data-ttu-id="73aed-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="73aed-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="73aed-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="73aed-144">OUTPUTS</span></span>

### <span data-ttu-id="73aed-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="73aed-145">System.Boolean</span></span>

## <span data-ttu-id="73aed-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="73aed-146">NOTES</span></span>

## <span data-ttu-id="73aed-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="73aed-147">RELATED LINKS</span></span>
