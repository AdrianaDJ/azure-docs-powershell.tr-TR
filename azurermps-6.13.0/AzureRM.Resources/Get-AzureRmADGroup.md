---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 85DDA491-7A7D-4217-B0E3-72CDC3787889
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADGroup.md
ms.openlocfilehash: 8dc8188d9408c1b8e37fe44b149ceebeaf12ee4c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590060"
---
# <span data-ttu-id="8d015-101">Get-AzureRmADGroup</span><span class="sxs-lookup"><span data-stu-id="8d015-101">Get-AzureRmADGroup</span></span>

## <span data-ttu-id="8d015-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d015-102">SYNOPSIS</span></span>
<span data-ttu-id="8d015-103">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="8d015-103">Filters active directory groups.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8d015-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8d015-104">SYNTAX</span></span>

### <span data-ttu-id="8d015-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8d015-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADGroup [-ObjectId <Guid>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8d015-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d015-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayNameStartsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8d015-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d015-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADGroup -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="8d015-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="8d015-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADGroup -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="8d015-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8d015-109">DESCRIPTION</span></span>
<span data-ttu-id="8d015-110">Active Directory gruplarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="8d015-110">Filters active directory groups.</span></span>

## <span data-ttu-id="8d015-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8d015-111">EXAMPLES</span></span>

### <span data-ttu-id="8d015-112">Örnek 1-tüm AD gruplarını listeler</span><span class="sxs-lookup"><span data-stu-id="8d015-112">Example 1 - List all AD groups</span></span>
```
PS C:\> Get-AzureRmADGroup
```

<span data-ttu-id="8d015-113">Kiracıdaki tüm AD gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="8d015-113">Lists all AD groups in a tenant.</span></span>

### <span data-ttu-id="8d015-114">Örnek 2-sayfalama kullanarak tüm AD gruplarını listeler</span><span class="sxs-lookup"><span data-stu-id="8d015-114">Example 2 - List all AD groups using paging</span></span>

```
PS C:\> Get-AzureRmADGroup -First 100
```

<span data-ttu-id="8d015-115">Kiracıdaki ilk 100 AD grubunu listeler.</span><span class="sxs-lookup"><span data-stu-id="8d015-115">Lists the first 100 AD groups in a tenant.</span></span>

### <span data-ttu-id="8d015-116">Örnek 3-nesne kimliğini by AD grubuna göre alma</span><span class="sxs-lookup"><span data-stu-id="8d015-116">Example 3 - Get AD group by object id</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="8d015-117">Nesne kimliği ' 85F89C90-780E-4AA6-9F4F-6F268VSEÇ322EEE ' olan bir AD grubunu alır.</span><span class="sxs-lookup"><span data-stu-id="8d015-117">Gets an AD group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="8d015-118">Örnek 4-arama dizesine göre gruplar</span><span class="sxs-lookup"><span data-stu-id="8d015-118">Example 4 - List groups by search string</span></span>

```
PS C:\> Get-AzureRmADGroup -SearchString Joe
```

<span data-ttu-id="8d015-119">Görünen adı ' Joe ' ile başlayan tüm AD gruplarını listeler.</span><span class="sxs-lookup"><span data-stu-id="8d015-119">Lists all AD groups whose display name begins with 'Joe'.</span></span>

## <span data-ttu-id="8d015-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8d015-120">PARAMETERS</span></span>

### <span data-ttu-id="8d015-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d015-121">-DefaultProfile</span></span>
<span data-ttu-id="8d015-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8d015-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d015-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8d015-123">-DisplayName</span></span>
<span data-ttu-id="8d015-124">Grubun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="8d015-124">The display name of the group.</span></span>

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

### <span data-ttu-id="8d015-125">-DisplayNameStartsWith</span><span class="sxs-lookup"><span data-stu-id="8d015-125">-DisplayNameStartsWith</span></span>
<span data-ttu-id="8d015-126">Sağlanan dizeyle başlayan grupları bulmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="8d015-126">Used to find groups that begin with the provided string.</span></span>

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

### <span data-ttu-id="8d015-127">-Önce</span><span class="sxs-lookup"><span data-stu-id="8d015-127">-First</span></span>
<span data-ttu-id="8d015-128">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="8d015-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="8d015-129">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="8d015-129">-IncludeTotalCount</span></span>
<span data-ttu-id="8d015-130">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="8d015-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="8d015-131">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="8d015-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="8d015-132">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8d015-132">-ObjectId</span></span>
<span data-ttu-id="8d015-133">Grubun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="8d015-133">Object id of the group.</span></span>

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

### <span data-ttu-id="8d015-134">-Atla</span><span class="sxs-lookup"><span data-stu-id="8d015-134">-Skip</span></span>
<span data-ttu-id="8d015-135">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="8d015-135">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="8d015-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d015-136">CommonParameters</span></span>
<span data-ttu-id="8d015-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8d015-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d015-138">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d015-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d015-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8d015-139">INPUTS</span></span>

### <span data-ttu-id="8d015-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8d015-140">System.String</span></span>

### <span data-ttu-id="8d015-141">System. Guid</span><span class="sxs-lookup"><span data-stu-id="8d015-141">System.Guid</span></span>

## <span data-ttu-id="8d015-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8d015-142">OUTPUTS</span></span>

### <span data-ttu-id="8d015-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="8d015-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="8d015-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8d015-144">NOTES</span></span>

## <span data-ttu-id="8d015-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8d015-145">RELATED LINKS</span></span>

[<span data-ttu-id="8d015-146">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="8d015-146">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="8d015-147">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8d015-147">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="8d015-148">Get-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="8d015-148">Get-AzureRmADGroupMember</span></span>](./Get-AzureRmADGroupMember.md)

