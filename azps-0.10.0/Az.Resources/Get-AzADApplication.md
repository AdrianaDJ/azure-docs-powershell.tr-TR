---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: 5f019f413e7ae0efa2013412499fcf34bd94a248
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936468"
---
# <span data-ttu-id="a9709-101">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a9709-101">Get-AzADApplication</span></span>

## <span data-ttu-id="a9709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9709-102">SYNOPSIS</span></span>
<span data-ttu-id="a9709-103">Var olan Azure Active Directory uygulamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="a9709-103">Lists existing azure active directory applications.</span></span>

## <span data-ttu-id="a9709-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a9709-104">SYNTAX</span></span>

### <span data-ttu-id="a9709-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a9709-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a9709-106">Applicationobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="a9709-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a9709-107">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="a9709-107">ApplicationIdParameterSet</span></span>
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a9709-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9709-108">SearchStringParameterSet</span></span>
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a9709-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9709-109">DisplayNameParameterSet</span></span>
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="a9709-110">Applicationıdentifieruriparameterset</span><span class="sxs-lookup"><span data-stu-id="a9709-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="a9709-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="a9709-111">DESCRIPTION</span></span>
<span data-ttu-id="a9709-112">Var olan Azure Active Directory uygulamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="a9709-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="a9709-113">Uygulama araması objectID, ApplicationId, ıdentifieruri veya DisplayName tarafından yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="a9709-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="a9709-114">Parametre sağlanmadıysa, kiracı altındaki tüm uygulamaları getirir.</span><span class="sxs-lookup"><span data-stu-id="a9709-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="a9709-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a9709-115">EXAMPLES</span></span>

### <span data-ttu-id="a9709-116">Örnek 1-tüm uygulamaları listeler</span><span class="sxs-lookup"><span data-stu-id="a9709-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzADApplication
```

<span data-ttu-id="a9709-117">Kiracı 'nın altındaki tüm uygulamaları listeler.</span><span class="sxs-lookup"><span data-stu-id="a9709-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="a9709-118">Örnek 2-sayfalama kullanarak uygulamaları listeleyin</span><span class="sxs-lookup"><span data-stu-id="a9709-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzADApplication -First 100
```

<span data-ttu-id="a9709-119">Kiracı 'nın altındaki ilk 100 uygulamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="a9709-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="a9709-120">Örnek 3-tanımlayıcı URI 'ye göre uygulama alın</span><span class="sxs-lookup"><span data-stu-id="a9709-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="a9709-121">URI değerini "" olarak alır http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="a9709-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="a9709-122">Örnek 4-nesne kimliğini kullanarak uygulamayı alın</span><span class="sxs-lookup"><span data-stu-id="a9709-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="a9709-123">Uygulama kimliği ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' olan uygulamayı alır.</span><span class="sxs-lookup"><span data-stu-id="a9709-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="a9709-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a9709-124">PARAMETERS</span></span>

### <span data-ttu-id="a9709-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a9709-125">-ApplicationId</span></span>
<span data-ttu-id="a9709-126">Getirilecek uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="a9709-126">The application id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9709-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9709-127">-DefaultProfile</span></span>
<span data-ttu-id="a9709-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a9709-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9709-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a9709-129">-DisplayName</span></span>
<span data-ttu-id="a9709-130">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="a9709-130">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9709-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="a9709-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="a9709-132">Görünen adla başlayan tüm uygulamaları getirir.</span><span class="sxs-lookup"><span data-stu-id="a9709-132">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9709-133">-Önce</span><span class="sxs-lookup"><span data-stu-id="a9709-133">-First</span></span>
<span data-ttu-id="a9709-134">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="a9709-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="a9709-135">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="a9709-135">-IdentifierUri</span></span>
<span data-ttu-id="a9709-136">Getirilecek uygulamanın benzersiz tanımlayıcı URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="a9709-136">Unique identifier Uri of the application to fetch.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9709-137">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="a9709-137">-IncludeTotalCount</span></span>
<span data-ttu-id="a9709-138">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="a9709-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="a9709-139">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="a9709-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="a9709-140">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="a9709-140">-ObjectId</span></span>
<span data-ttu-id="a9709-141">Getirilecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="a9709-141">The object id of the application to fetch.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9709-142">-Atla</span><span class="sxs-lookup"><span data-stu-id="a9709-142">-Skip</span></span>
<span data-ttu-id="a9709-143">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="a9709-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="a9709-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9709-144">CommonParameters</span></span>
<span data-ttu-id="a9709-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a9709-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9709-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9709-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9709-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a9709-147">INPUTS</span></span>

### <span data-ttu-id="a9709-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="a9709-148">System.Guid</span></span>

### <span data-ttu-id="a9709-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a9709-149">System.String</span></span>

## <span data-ttu-id="a9709-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a9709-150">OUTPUTS</span></span>

### <span data-ttu-id="a9709-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="a9709-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="a9709-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a9709-152">NOTES</span></span>

## <span data-ttu-id="a9709-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a9709-153">RELATED LINKS</span></span>

[<span data-ttu-id="a9709-154">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a9709-154">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="a9709-155">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a9709-155">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="a9709-156">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="a9709-156">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="a9709-157">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a9709-157">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="a9709-158">Set-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a9709-158">Set-AzADApplication</span></span>](./Set-AzADApplication.md)

[<span data-ttu-id="a9709-159">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="a9709-159">New-AzADApplication</span></span>](./New-AzADApplication.md)

