---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
ms.openlocfilehash: 9ddc9658d6d18cc7a08df33f1f976521656c9234
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939248"
---
# <span data-ttu-id="451b5-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="451b5-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="451b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="451b5-102">SYNOPSIS</span></span>
<span data-ttu-id="451b5-103">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="451b5-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="451b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="451b5-104">SYNTAX</span></span>

### <span data-ttu-id="451b5-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="451b5-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="451b5-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="451b5-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="451b5-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="451b5-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="451b5-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="451b5-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="451b5-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="451b5-109">DESCRIPTION</span></span>
<span data-ttu-id="451b5-110">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="451b5-110">Filters active directory groups.</span></span>

## <span data-ttu-id="451b5-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="451b5-111">EXAMPLES</span></span>

### <span data-ttu-id="451b5-112">Örnek 1-tüm AD gruplarını listeler</span><span class="sxs-lookup"><span data-stu-id="451b5-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="451b5-113">Kiracıdaki tüm AD gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="451b5-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="451b5-114">Örnek 2-sayfalama kullanarak tüm AD gruplarını listeler</span><span class="sxs-lookup"><span data-stu-id="451b5-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="451b5-115">Kiracıdaki ilk 100 AD grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="451b5-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="451b5-116">Örnek 3-nesne kimliğini by AD grubuna göre alma</span><span class="sxs-lookup"><span data-stu-id="451b5-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="451b5-117">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan bir AD grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="451b5-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="451b5-118">Örnek 4-arama dizesine göre gruplar</span><span class="sxs-lookup"><span data-stu-id="451b5-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="451b5-119">Görünen adı ' Joe ' ile başlayan tüm AD gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="451b5-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="451b5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="451b5-120">PARAMETERS</span></span>

### <span data-ttu-id="451b5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="451b5-121">-DefaultProfile</span></span>
<span data-ttu-id="451b5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="451b5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="451b5-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="451b5-123">-DisplayName</span></span>
<span data-ttu-id="451b5-124">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="451b5-124">The display name of the group.</span></span>

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

### <span data-ttu-id="451b5-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="451b5-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="451b5-126">Sağlanan dizeyle başlayan grupları bulmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="451b5-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="451b5-127">-Önce</span><span class="sxs-lookup"><span data-stu-id="451b5-127">-First</span></span>
<span data-ttu-id="451b5-128">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="451b5-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="451b5-129">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="451b5-129">-IncludeTotalCount</span></span>
<span data-ttu-id="451b5-130">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="451b5-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="451b5-131">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="451b5-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="451b5-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="451b5-132">-ObjectId</span></span>
<span data-ttu-id="451b5-133">Grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="451b5-133">Object id of the group.</span></span>

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

### <span data-ttu-id="451b5-134">-Atla</span><span class="sxs-lookup"><span data-stu-id="451b5-134">-Skip</span></span>
<span data-ttu-id="451b5-135">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="451b5-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="451b5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="451b5-136">CommonParameters</span></span>
<span data-ttu-id="451b5-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="451b5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="451b5-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="451b5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="451b5-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="451b5-139">INPUTS</span></span>

### <span data-ttu-id="451b5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="451b5-140">System.String</span></span>

### <span data-ttu-id="451b5-141">System. Guid</span><span class="sxs-lookup"><span data-stu-id="451b5-141">System.Guid</span></span>

## <span data-ttu-id="451b5-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="451b5-142">OUTPUTS</span></span>

### <span data-ttu-id="451b5-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="451b5-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="451b5-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="451b5-144">NOTES</span></span>

## <span data-ttu-id="451b5-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="451b5-145">RELATED LINKS</span></span>

[<span data-ttu-id="451b5-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="451b5-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="451b5-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="451b5-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="451b5-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="451b5-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

