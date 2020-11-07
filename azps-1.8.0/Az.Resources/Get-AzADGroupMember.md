---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroupMember.md
ms.openlocfilehash: 25de035b853d1a17ee06a7efb6ac31631bd466f8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759453"
---
# <span data-ttu-id="5d99e-101">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="5d99e-101">Get-AzADGroupMember</span></span>

## <span data-ttu-id="5d99e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d99e-102">SYNOPSIS</span></span>
<span data-ttu-id="5d99e-103">Geçerli Kiracıdaki bir AD grubunun üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="5d99e-103">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="5d99e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5d99e-104">SYNTAX</span></span>

### <span data-ttu-id="5d99e-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5d99e-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzADGroupMember [-GroupObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5d99e-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d99e-106">DisplayNameParameterSet</span></span>
```
Get-AzADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="5d99e-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d99e-107">GroupObjectParameterSet</span></span>
```
Get-AzADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="5d99e-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5d99e-108">DESCRIPTION</span></span>
<span data-ttu-id="5d99e-109">Geçerli Kiracıdaki bir AD grubunun üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="5d99e-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="5d99e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5d99e-110">EXAMPLES</span></span>

### <span data-ttu-id="5d99e-111">Örnek 1-AD grubu nesne kimliğine göre üyeleri listeler</span><span class="sxs-lookup"><span data-stu-id="5d99e-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="5d99e-112">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan AD grubunun üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="5d99e-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5d99e-113">Örnek 2-sayfalama kullanarak AD grubu nesne kimliğine göre üyeleri listeler</span><span class="sxs-lookup"><span data-stu-id="5d99e-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="5d99e-114">AD grubunun ilk 100 üyesini nesne kimliği ' 85f89c90-780e-4aa6-9F</span><span class="sxs-lookup"><span data-stu-id="5d99e-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="5d99e-115">Örnek 3-boruları göre üyeleri Listele</span><span class="sxs-lookup"><span data-stu-id="5d99e-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzADGroupMember
```

<span data-ttu-id="5d99e-116">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve Get-AzADGroupMember yöneltmeleri</span><span class="sxs-lookup"><span data-stu-id="5d99e-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="5d99e-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5d99e-117">PARAMETERS</span></span>

### <span data-ttu-id="5d99e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d99e-118">-DefaultProfile</span></span>
<span data-ttu-id="5d99e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="5d99e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d99e-120">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="5d99e-120">-GroupDisplayName</span></span>
<span data-ttu-id="5d99e-121">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="5d99e-121">The display name of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d99e-122">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="5d99e-122">-GroupObject</span></span>
<span data-ttu-id="5d99e-123">Üyelerini listeleyen Grup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="5d99e-123">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d99e-124">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="5d99e-124">-GroupObjectId</span></span>
<span data-ttu-id="5d99e-125">Grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="5d99e-125">Object Id of the group.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d99e-126">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="5d99e-126">-IncludeTotalCount</span></span>
<span data-ttu-id="5d99e-127">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="5d99e-127">Reports the number of objects in the data set.</span></span> <span data-ttu-id="5d99e-128">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="5d99e-128">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="5d99e-129">-Atla</span><span class="sxs-lookup"><span data-stu-id="5d99e-129">-Skip</span></span>
<span data-ttu-id="5d99e-130">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="5d99e-130">Ignores the first N objects and then gets the remaining objects.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d99e-131">-Önce</span><span class="sxs-lookup"><span data-stu-id="5d99e-131">-First</span></span>
<span data-ttu-id="5d99e-132">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="5d99e-132">The maximum number of objects to return.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d99e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d99e-133">CommonParameters</span></span>
<span data-ttu-id="5d99e-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5d99e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d99e-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d99e-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d99e-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5d99e-136">INPUTS</span></span>

### <span data-ttu-id="5d99e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5d99e-137">System.String</span></span>

### <span data-ttu-id="5d99e-138">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="5d99e-138">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="5d99e-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5d99e-139">OUTPUTS</span></span>

### <span data-ttu-id="5d99e-140">Microsoft. Azure. Commands. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="5d99e-140">Microsoft.Azure.Commands.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="5d99e-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5d99e-141">NOTES</span></span>

## <span data-ttu-id="5d99e-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5d99e-142">RELATED LINKS</span></span>

[<span data-ttu-id="5d99e-143">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="5d99e-143">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="5d99e-144">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5d99e-144">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

