---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 42696be07c560d24d1d87542873b6795497c370c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936461"
---
# <span data-ttu-id="69549-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="69549-101">Get-AzADGroup</span></span>

## <span data-ttu-id="69549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69549-102">SYNOPSIS</span></span>
<span data-ttu-id="69549-103">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="69549-103">Filters active directory groups.</span></span>

## <span data-ttu-id="69549-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="69549-104">SYNTAX</span></span>

### <span data-ttu-id="69549-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="69549-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="69549-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="69549-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="69549-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69549-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="69549-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="69549-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="69549-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="69549-109">DESCRIPTION</span></span>
<span data-ttu-id="69549-110">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="69549-110">Filters active directory groups.</span></span>

## <span data-ttu-id="69549-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="69549-111">EXAMPLES</span></span>

### <span data-ttu-id="69549-112">Örnek 1-tüm AD gruplarını listeler</span><span class="sxs-lookup"><span data-stu-id="69549-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzADGroup
```

<span data-ttu-id="69549-113">Kiracıdaki tüm AD gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="69549-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="69549-114">Örnek 2-sayfalama kullanarak tüm AD gruplarını listeler</span><span class="sxs-lookup"><span data-stu-id="69549-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="69549-115">Kiracıdaki ilk 100 AD grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="69549-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="69549-116">Örnek 3-nesne kimliğini by AD grubuna göre alma</span><span class="sxs-lookup"><span data-stu-id="69549-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="69549-117">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan bir AD grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="69549-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="69549-118">Örnek 4-arama dizesine göre gruplar</span><span class="sxs-lookup"><span data-stu-id="69549-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="69549-119">Görünen adı ' Joe ' ile başlayan tüm AD gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="69549-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="69549-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="69549-120">PARAMETERS</span></span>

### <span data-ttu-id="69549-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69549-121">-DefaultProfile</span></span>
<span data-ttu-id="69549-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="69549-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69549-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="69549-123">-DisplayName</span></span>
<span data-ttu-id="69549-124">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="69549-124">The display name of the group.</span></span>

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

### <span data-ttu-id="69549-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="69549-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="69549-126">Sağlanan dizeyle başlayan grupları bulmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="69549-126">Used to find groups that begin with the provided string.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69549-127">-Önce</span><span class="sxs-lookup"><span data-stu-id="69549-127">-First</span></span>
<span data-ttu-id="69549-128">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="69549-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="69549-129">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="69549-129">-IncludeTotalCount</span></span>
<span data-ttu-id="69549-130">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="69549-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="69549-131">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="69549-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="69549-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="69549-132">-ObjectId</span></span>
<span data-ttu-id="69549-133">Grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="69549-133">Object id of the group.</span></span>

```yaml
Type: System.Guid
Parameter Sets: EmptyParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69549-134">-Atla</span><span class="sxs-lookup"><span data-stu-id="69549-134">-Skip</span></span>
<span data-ttu-id="69549-135">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="69549-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="69549-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69549-136">CommonParameters</span></span>
<span data-ttu-id="69549-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="69549-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69549-138">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69549-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69549-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="69549-139">INPUTS</span></span>

### <span data-ttu-id="69549-140">System. String</span><span class="sxs-lookup"><span data-stu-id="69549-140">System.String</span></span>

### <span data-ttu-id="69549-141">System. Guid</span><span class="sxs-lookup"><span data-stu-id="69549-141">System.Guid</span></span>

## <span data-ttu-id="69549-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="69549-142">OUTPUTS</span></span>

### <span data-ttu-id="69549-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="69549-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="69549-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="69549-144">NOTES</span></span>

## <span data-ttu-id="69549-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="69549-145">RELATED LINKS</span></span>

[<span data-ttu-id="69549-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="69549-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="69549-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="69549-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="69549-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="69549-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

