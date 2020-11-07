---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADGroup.md
ms.openlocfilehash: 63c08b038c1c225cd1e1afe188bb70c6b044251e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759460"
---
# <span data-ttu-id="52f67-101">Get-AzADGroup</span><span class="sxs-lookup"><span data-stu-id="52f67-101">Get-AzADGroup</span></span>

## <span data-ttu-id="52f67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52f67-102">SYNOPSIS</span></span>
<span data-ttu-id="52f67-103">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="52f67-103">Filters active directory groups.</span></span>

## <span data-ttu-id="52f67-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="52f67-104">SYNTAX</span></span>

### <span data-ttu-id="52f67-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="52f67-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="52f67-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="52f67-106">SearchStringParameterSet</span></span>
```
Get-AzADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="52f67-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="52f67-107">DisplayNameParameterSet</span></span>
```
Get-AzADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="52f67-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="52f67-108">ObjectIdParameterSet</span></span>
```
Get-AzADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="52f67-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="52f67-109">DESCRIPTION</span></span>
<span data-ttu-id="52f67-110">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="52f67-110">Filters active directory groups.</span></span>

## <span data-ttu-id="52f67-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="52f67-111">EXAMPLES</span></span>

### <span data-ttu-id="52f67-112">Örnek 1-tüm AD gruplarını listeler</span><span class="sxs-lookup"><span data-stu-id="52f67-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzADGroup
```

<span data-ttu-id="52f67-113">Kiracıdaki tüm AD gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="52f67-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="52f67-114">Örnek 2-sayfalama kullanarak tüm AD gruplarını listeler</span><span class="sxs-lookup"><span data-stu-id="52f67-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzADGroup -First 100
```

<span data-ttu-id="52f67-115">Kiracıdaki ilk 100 AD grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="52f67-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="52f67-116">Örnek 3-nesne kimliğini by AD grubuna göre alma</span><span class="sxs-lookup"><span data-stu-id="52f67-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="52f67-117">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan bir AD grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="52f67-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="52f67-118">Örnek 4-arama dizesine göre gruplar</span><span class="sxs-lookup"><span data-stu-id="52f67-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzADGroup -SearchString Joe
```

<span data-ttu-id="52f67-119">Görünen adı ' Joe ' ile başlayan tüm AD gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="52f67-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="52f67-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="52f67-120">PARAMETERS</span></span>

### <span data-ttu-id="52f67-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f67-121">-DefaultProfile</span></span>
<span data-ttu-id="52f67-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="52f67-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52f67-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="52f67-123">-DisplayName</span></span>
<span data-ttu-id="52f67-124">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="52f67-124">The display name of the group.</span></span>

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

### <span data-ttu-id="52f67-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="52f67-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="52f67-126">Sağlanan dizeyle başlayan grupları bulmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="52f67-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="52f67-127">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="52f67-127">-ObjectId</span></span>
<span data-ttu-id="52f67-128">Grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="52f67-128">Object id of the group.</span></span>

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

### <span data-ttu-id="52f67-129">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="52f67-129">-IncludeTotalCount</span></span>
<span data-ttu-id="52f67-130">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="52f67-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="52f67-131">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="52f67-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="52f67-132">-Atla</span><span class="sxs-lookup"><span data-stu-id="52f67-132">-Skip</span></span>
<span data-ttu-id="52f67-133">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="52f67-133">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="52f67-134">-Önce</span><span class="sxs-lookup"><span data-stu-id="52f67-134">-First</span></span>
<span data-ttu-id="52f67-135">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="52f67-135">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="52f67-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f67-136">CommonParameters</span></span>
<span data-ttu-id="52f67-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="52f67-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f67-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f67-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f67-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="52f67-139">INPUTS</span></span>

### <span data-ttu-id="52f67-140">System. String</span><span class="sxs-lookup"><span data-stu-id="52f67-140">System.String</span></span>

### <span data-ttu-id="52f67-141">System. Guid</span><span class="sxs-lookup"><span data-stu-id="52f67-141">System.Guid</span></span>

## <span data-ttu-id="52f67-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="52f67-142">OUTPUTS</span></span>

### <span data-ttu-id="52f67-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="52f67-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="52f67-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="52f67-144">NOTES</span></span>

## <span data-ttu-id="52f67-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="52f67-145">RELATED LINKS</span></span>

[<span data-ttu-id="52f67-146">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="52f67-146">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="52f67-147">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="52f67-147">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="52f67-148">Get-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="52f67-148">Get-AzADGroupMember</span></span>](./Get-AzADGroupMember.md)

