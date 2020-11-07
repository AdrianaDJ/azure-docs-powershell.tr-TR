---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 34a00ed29d40d8824ac0f2d24f5275bb7c0a0164
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936457"
---
# <span data-ttu-id="42182-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="42182-101">Get-AzADUser</span></span>

## <span data-ttu-id="42182-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42182-102">SYNOPSIS</span></span>
<span data-ttu-id="42182-103">Active Directory kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="42182-103">Filters active directory users.</span></span>

## <span data-ttu-id="42182-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="42182-104">SYNTAX</span></span>

### <span data-ttu-id="42182-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="42182-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="42182-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="42182-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="42182-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="42182-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="42182-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="42182-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="42182-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="42182-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="42182-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="42182-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="42182-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="42182-111">DESCRIPTION</span></span>
<span data-ttu-id="42182-112">Active Directory kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="42182-112">Filters active directory users.</span></span>

## <span data-ttu-id="42182-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="42182-113">EXAMPLES</span></span>

### <span data-ttu-id="42182-114">Örnek 1-tüm kullanıcıları listeler</span><span class="sxs-lookup"><span data-stu-id="42182-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="42182-115">Kiracıdaki tüm reklam kullanıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="42182-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="42182-116">Örnek 2-sayfalama kullanan tüm kullanıcıları listeler</span><span class="sxs-lookup"><span data-stu-id="42182-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="42182-117">Kiracıdaki ilk 100 AD kullanıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="42182-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="42182-118">Örnek 3-Kullanıcı asıl adına göre AD kullanıcısını alma</span><span class="sxs-lookup"><span data-stu-id="42182-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="42182-119">AD kullanıcısını Kullanıcı asıl adı "" ile alır foo@domain.com .</span><span class="sxs-lookup"><span data-stu-id="42182-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="42182-120">Örnek 4-arama dizesine göre liste</span><span class="sxs-lookup"><span data-stu-id="42182-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="42182-121">Görünen adı "Joe" ile başlayan tüm AD kullanıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="42182-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="42182-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="42182-122">PARAMETERS</span></span>

### <span data-ttu-id="42182-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42182-123">-DefaultProfile</span></span>
<span data-ttu-id="42182-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="42182-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42182-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="42182-125">-DisplayName</span></span>
<span data-ttu-id="42182-126">Kullanıcının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="42182-126">The display name of the user.</span></span>

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

### <span data-ttu-id="42182-127">-Önce</span><span class="sxs-lookup"><span data-stu-id="42182-127">-First</span></span>
<span data-ttu-id="42182-128">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="42182-128">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="42182-129">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="42182-129">-IncludeTotalCount</span></span>
<span data-ttu-id="42182-130">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="42182-130">Reports the number of objects in the data set.</span></span> <span data-ttu-id="42182-131">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="42182-131">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="42182-132">-Posta</span><span class="sxs-lookup"><span data-stu-id="42182-132">-Mail</span></span>
<span data-ttu-id="42182-133">Kullanıcı postası.</span><span class="sxs-lookup"><span data-stu-id="42182-133">The user mail.</span></span>

```yaml
Type: System.String
Parameter Sets: MailParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42182-134">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="42182-134">-ObjectId</span></span>
<span data-ttu-id="42182-135">Kullanıcının nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="42182-135">Object id of the user.</span></span>

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

### <span data-ttu-id="42182-136">-Atla</span><span class="sxs-lookup"><span data-stu-id="42182-136">-Skip</span></span>
<span data-ttu-id="42182-137">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="42182-137">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="42182-138">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="42182-138">-StartsWith</span></span>
<span data-ttu-id="42182-139">Sağlanan dizeyle başlayan kullanıcıları bulmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="42182-139">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="42182-140">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="42182-140">-UserPrincipalName</span></span>
<span data-ttu-id="42182-141">Kullanıcının UPN 'si.</span><span class="sxs-lookup"><span data-stu-id="42182-141">UPN of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: EmptyParameterSet
Aliases: UPN

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UPNParameterSet
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42182-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42182-142">CommonParameters</span></span>
<span data-ttu-id="42182-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="42182-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42182-144">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42182-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42182-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="42182-145">INPUTS</span></span>

### <span data-ttu-id="42182-146">System. String</span><span class="sxs-lookup"><span data-stu-id="42182-146">System.String</span></span>

### <span data-ttu-id="42182-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="42182-147">System.Guid</span></span>

## <span data-ttu-id="42182-148">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="42182-148">OUTPUTS</span></span>

### <span data-ttu-id="42182-149">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="42182-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="42182-150">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="42182-150">NOTES</span></span>

## <span data-ttu-id="42182-151">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="42182-151">RELATED LINKS</span></span>

[<span data-ttu-id="42182-152">Yeni-AzADUser</span><span class="sxs-lookup"><span data-stu-id="42182-152">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="42182-153">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="42182-153">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="42182-154">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="42182-154">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

