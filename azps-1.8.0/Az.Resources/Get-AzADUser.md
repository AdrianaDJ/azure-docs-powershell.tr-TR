---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BF254F2F-F658-45CC-8AC8-53FF96CFCAAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADUser.md
ms.openlocfilehash: 910df03db722636e91e95ff1c6aad7898b333740
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759448"
---
# <span data-ttu-id="76038-101">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="76038-101">Get-AzADUser</span></span>

## <span data-ttu-id="76038-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76038-102">SYNOPSIS</span></span>
<span data-ttu-id="76038-103">Active Directory kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="76038-103">Filters active directory users.</span></span>

## <span data-ttu-id="76038-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="76038-104">SYNTAX</span></span>

### <span data-ttu-id="76038-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="76038-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADUser [-UserPrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="76038-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="76038-106">SearchStringParameterSet</span></span>
```
Get-AzADUser -StartsWith <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="76038-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="76038-107">DisplayNameParameterSet</span></span>
```
Get-AzADUser -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="76038-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="76038-108">ObjectIdParameterSet</span></span>
```
Get-AzADUser -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="76038-109">UPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="76038-109">UPNParameterSet</span></span>
```
Get-AzADUser -UserPrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="76038-110">MailParameterSet</span><span class="sxs-lookup"><span data-stu-id="76038-110">MailParameterSet</span></span>
```
Get-AzADUser -Mail <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="76038-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="76038-111">DESCRIPTION</span></span>
<span data-ttu-id="76038-112">Active Directory kullanıcılarına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="76038-112">Filters active directory users.</span></span>

## <span data-ttu-id="76038-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="76038-113">EXAMPLES</span></span>

### <span data-ttu-id="76038-114">Örnek 1-tüm kullanıcıları listeler</span><span class="sxs-lookup"><span data-stu-id="76038-114">Example 1 - List all users</span></span>

```
PS C:\> Get-AzADUser
```

<span data-ttu-id="76038-115">Kiracıdaki tüm reklam kullanıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="76038-115">Lists all AD users in a tenant.</span></span>

### <span data-ttu-id="76038-116">Örnek 2-sayfalama kullanan tüm kullanıcıları listeler</span><span class="sxs-lookup"><span data-stu-id="76038-116">Example 2 - List all users using paging</span></span>

```
PS C:\> Get-AzADUser -First 100
```

<span data-ttu-id="76038-117">Kiracıdaki ilk 100 AD kullanıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="76038-117">Lists the first 100 AD users in a tenant.</span></span>

### <span data-ttu-id="76038-118">Örnek 3-Kullanıcı asıl adına göre AD kullanıcısını alma</span><span class="sxs-lookup"><span data-stu-id="76038-118">Example 3 - Get AD user by user principal name</span></span>

```
PS C:\> Get-AzADUser -UserPrincipalName foo@domain.com
```

<span data-ttu-id="76038-119">AD kullanıcısını Kullanıcı asıl adı "" ile alır foo@domain.com .</span><span class="sxs-lookup"><span data-stu-id="76038-119">Gets the AD user with user principal name "foo@domain.com".</span></span>

### <span data-ttu-id="76038-120">Örnek 4-arama dizesine göre liste</span><span class="sxs-lookup"><span data-stu-id="76038-120">Example 4 - List by search string</span></span>

```
PS C:\> Get-AzADUser -SearchString Joe
```

<span data-ttu-id="76038-121">Görünen adı "Joe" ile başlayan tüm AD kullanıcılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="76038-121">Lists all AD users whose display name starts with "Joe".</span></span>

## <span data-ttu-id="76038-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="76038-122">PARAMETERS</span></span>

### <span data-ttu-id="76038-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76038-123">-DefaultProfile</span></span>
<span data-ttu-id="76038-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="76038-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76038-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="76038-125">-DisplayName</span></span>
<span data-ttu-id="76038-126">Kullanıcının görünen adı.</span><span class="sxs-lookup"><span data-stu-id="76038-126">The display name of the user.</span></span>

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

### <span data-ttu-id="76038-127">-Posta</span><span class="sxs-lookup"><span data-stu-id="76038-127">-Mail</span></span>
<span data-ttu-id="76038-128">Kullanıcı postası.</span><span class="sxs-lookup"><span data-stu-id="76038-128">The user mail.</span></span>

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

### <span data-ttu-id="76038-129">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="76038-129">-ObjectId</span></span>
<span data-ttu-id="76038-130">Kullanıcının nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="76038-130">Object id of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76038-131">-StartsWith</span><span class="sxs-lookup"><span data-stu-id="76038-131">-StartsWith</span></span>
<span data-ttu-id="76038-132">Sağlanan dizeyle başlayan kullanıcıları bulmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="76038-132">Used to find users that begin with the provided string.</span></span>

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

### <span data-ttu-id="76038-133">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="76038-133">-UserPrincipalName</span></span>
<span data-ttu-id="76038-134">Kullanıcının UPN 'si.</span><span class="sxs-lookup"><span data-stu-id="76038-134">UPN of the user.</span></span>

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

### <span data-ttu-id="76038-135">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="76038-135">-IncludeTotalCount</span></span>
<span data-ttu-id="76038-136">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="76038-136">Reports the number of objects in the data set.</span></span> <span data-ttu-id="76038-137">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="76038-137">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="76038-138">-Atla</span><span class="sxs-lookup"><span data-stu-id="76038-138">-Skip</span></span>
<span data-ttu-id="76038-139">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="76038-139">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="76038-140">-Önce</span><span class="sxs-lookup"><span data-stu-id="76038-140">-First</span></span>
<span data-ttu-id="76038-141">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="76038-141">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="76038-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76038-142">CommonParameters</span></span>
<span data-ttu-id="76038-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="76038-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76038-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76038-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76038-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="76038-145">INPUTS</span></span>

### <span data-ttu-id="76038-146">System. String</span><span class="sxs-lookup"><span data-stu-id="76038-146">System.String</span></span>

## <span data-ttu-id="76038-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="76038-147">OUTPUTS</span></span>

### <span data-ttu-id="76038-148">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="76038-148">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="76038-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="76038-149">NOTES</span></span>

## <span data-ttu-id="76038-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="76038-150">RELATED LINKS</span></span>

[<span data-ttu-id="76038-151">Yeni-AzADUser</span><span class="sxs-lookup"><span data-stu-id="76038-151">New-AzADUser</span></span>](./New-AzADUser.md)

[<span data-ttu-id="76038-152">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="76038-152">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="76038-153">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="76038-153">Remove-AzADUser</span></span>](./Remove-AzADUser.md)

