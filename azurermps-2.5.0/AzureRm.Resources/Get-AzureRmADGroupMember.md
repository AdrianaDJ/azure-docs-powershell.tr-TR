---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 52C5CD8B-2489-4FE6-9F33-B3350531CD8E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroupmember
schema: 2.0.0
ms.openlocfilehash: f790266f1e61446cb9d1c257929cf8b6e3ab25d3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939247"
---
# <span data-ttu-id="e9985-101">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="e9985-101">Get-AzureRmADGroupMember</span></span>

## <span data-ttu-id="e9985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9985-102">SYNOPSIS</span></span>
<span data-ttu-id="e9985-103">Geçerli Kiracıdaki bir AD grubunun üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="e9985-103">Lists members of an AD group in the current tenant.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9985-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e9985-104">SYNTAX</span></span>

### <span data-ttu-id="e9985-105">Objectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e9985-105">ObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADGroupMember [-GroupObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e9985-106">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9985-106">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupDisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="e9985-107">GroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9985-107">GroupObjectParameterSet</span></span>
```
Get-AzureRmADGroupMember -GroupObject <PSADGroup> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="e9985-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e9985-108">DESCRIPTION</span></span>
<span data-ttu-id="e9985-109">Geçerli Kiracıdaki bir AD grubunun üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="e9985-109">Lists members of an AD group in the current tenant.</span></span>

## <span data-ttu-id="e9985-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e9985-110">EXAMPLES</span></span>

### <span data-ttu-id="e9985-111">Örnek 1-AD grubu nesne kimliğine göre üyeleri listeler</span><span class="sxs-lookup"><span data-stu-id="e9985-111">Example 1 - List members by AD group object id</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="e9985-112">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan AD grubunun üyelerini listeler.</span><span class="sxs-lookup"><span data-stu-id="e9985-112">Lists members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e9985-113">Örnek 2-sayfalama kullanarak AD grubu nesne kimliğine göre üyeleri listeler</span><span class="sxs-lookup"><span data-stu-id="e9985-113">Example 2 - List members by AD group object id using paging</span></span>

```
PS C:\> Get-AzureRmADGroupMember -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE -First 100
```

<span data-ttu-id="e9985-114">AD grubunun ilk 100 üyesini nesne kimliği ' 85f89c90-780e-4aa6-9F</span><span class="sxs-lookup"><span data-stu-id="e9985-114">Lists the first 100 members of the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="e9985-115">Örnek 3-boruları göre üyeleri Listele</span><span class="sxs-lookup"><span data-stu-id="e9985-115">Example 3 - List members by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Get-AzureRmADGroupMember
```

<span data-ttu-id="e9985-116">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' ve Get-AzureRmADGroupMember yöneltmeleri</span><span class="sxs-lookup"><span data-stu-id="e9985-116">Gets the AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Get-AzureRmADGroupMember cmdlet to list all members in that group.</span></span> 

## <span data-ttu-id="e9985-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e9985-117">PARAMETERS</span></span>

### <span data-ttu-id="e9985-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9985-118">-DefaultProfile</span></span>
<span data-ttu-id="e9985-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e9985-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9985-120">-Önce</span><span class="sxs-lookup"><span data-stu-id="e9985-120">-First</span></span>
<span data-ttu-id="e9985-121">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="e9985-121">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="e9985-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="e9985-122">-GroupDisplayName</span></span>
<span data-ttu-id="e9985-123">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="e9985-123">The display name of the group.</span></span>

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

### <span data-ttu-id="e9985-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="e9985-124">-GroupObject</span></span>
<span data-ttu-id="e9985-125">Üyelerini listeleyen Grup nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e9985-125">The group object that you are listing members from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: GroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e9985-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="e9985-126">-GroupObjectId</span></span>
<span data-ttu-id="e9985-127">Grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="e9985-127">Object Id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases: Id, ObjectId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9985-128">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="e9985-128">-IncludeTotalCount</span></span>
<span data-ttu-id="e9985-129">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="e9985-129">Reports the number of objects in the data set.</span></span> <span data-ttu-id="e9985-130">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="e9985-130">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="e9985-131">-Atla</span><span class="sxs-lookup"><span data-stu-id="e9985-131">-Skip</span></span>
<span data-ttu-id="e9985-132">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="e9985-132">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="e9985-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9985-133">CommonParameters</span></span>
<span data-ttu-id="e9985-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e9985-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9985-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9985-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9985-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e9985-136">INPUTS</span></span>

### <span data-ttu-id="e9985-137">System. Guid</span><span class="sxs-lookup"><span data-stu-id="e9985-137">System.Guid</span></span>

### <span data-ttu-id="e9985-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="e9985-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="e9985-139">Parametreler: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e9985-139">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="e9985-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e9985-140">OUTPUTS</span></span>

### <span data-ttu-id="e9985-141">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADObject</span><span class="sxs-lookup"><span data-stu-id="e9985-141">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADObject</span></span>

## <span data-ttu-id="e9985-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e9985-142">NOTES</span></span>

## <span data-ttu-id="e9985-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e9985-143">RELATED LINKS</span></span>

[<span data-ttu-id="e9985-144">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="e9985-144">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="e9985-145">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="e9985-145">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

