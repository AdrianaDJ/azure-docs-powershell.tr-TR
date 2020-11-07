---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 4e7abd4a3b33f54e5a0ec0bdde01e3fe11da31c4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939249"
---
# <span data-ttu-id="c5420-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c5420-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="c5420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5420-102">SYNOPSIS</span></span>
<span data-ttu-id="c5420-103">Var olan Azure Active Directory uygulamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="c5420-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5420-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5420-104">SYNTAX</span></span>

### <span data-ttu-id="c5420-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c5420-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5420-106">Applicationobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="c5420-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5420-107">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c5420-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5420-108">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5420-108">SearchStringParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5420-109">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c5420-109">DisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="c5420-110">Applicationıdentifieruriparameterset</span><span class="sxs-lookup"><span data-stu-id="c5420-110">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="c5420-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5420-111">DESCRIPTION</span></span>
<span data-ttu-id="c5420-112">Var olan Azure Active Directory uygulamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="c5420-112">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="c5420-113">Uygulama araması objectID, ApplicationId, ıdentifieruri veya DisplayName tarafından yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="c5420-113">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="c5420-114">Parametre sağlanmadıysa, kiracı altındaki tüm uygulamaları getirir.</span><span class="sxs-lookup"><span data-stu-id="c5420-114">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="c5420-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5420-115">EXAMPLES</span></span>

### <span data-ttu-id="c5420-116">Örnek 1-tüm uygulamaları listeler</span><span class="sxs-lookup"><span data-stu-id="c5420-116">Example 1 - List all applications</span></span>

```
PS C:\> Get-AzureRmADApplication
```

<span data-ttu-id="c5420-117">Kiracı 'nın altındaki tüm uygulamaları listeler.</span><span class="sxs-lookup"><span data-stu-id="c5420-117">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="c5420-118">Örnek 2-sayfalama kullanarak uygulamaları listeleyin</span><span class="sxs-lookup"><span data-stu-id="c5420-118">Example 2 - List applications using paging</span></span>

```
PS C:\> Get-AzureRmADApplication -First 100
```

<span data-ttu-id="c5420-119">Kiracı 'nın altındaki ilk 100 uygulamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="c5420-119">Lists the first 100 applications under a tenant.</span></span>

### <span data-ttu-id="c5420-120">Örnek 3-tanımlayıcı URI 'ye göre uygulama alın</span><span class="sxs-lookup"><span data-stu-id="c5420-120">Example 3 - Get application by identifier URI</span></span>

```
PS C:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="c5420-121">URI değerini "" olarak alır http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="c5420-121">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

### <span data-ttu-id="c5420-122">Örnek 4-nesne kimliğini kullanarak uygulamayı alın</span><span class="sxs-lookup"><span data-stu-id="c5420-122">Example 4 - Get application by object id</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

<span data-ttu-id="c5420-123">Uygulama kimliği ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' olan uygulamayı alır.</span><span class="sxs-lookup"><span data-stu-id="c5420-123">Gets the application with the object id '39e64ec6-569b-4030-8e1c-c3c519a05d69'.</span></span>

## <span data-ttu-id="c5420-124">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5420-124">PARAMETERS</span></span>

### <span data-ttu-id="c5420-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c5420-125">-ApplicationId</span></span>
<span data-ttu-id="c5420-126">Getirilecek uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="c5420-126">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="c5420-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5420-127">-DefaultProfile</span></span>
<span data-ttu-id="c5420-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c5420-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5420-129">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c5420-129">-DisplayName</span></span>
<span data-ttu-id="c5420-130">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="c5420-130">The display name of the application.</span></span>

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

### <span data-ttu-id="c5420-131">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="c5420-131">-DisplayNameStartWith</span></span>
<span data-ttu-id="c5420-132">Görünen adla başlayan tüm uygulamaları getirir.</span><span class="sxs-lookup"><span data-stu-id="c5420-132">Fetch all applications starting with the display name.</span></span>

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

### <span data-ttu-id="c5420-133">-Önce</span><span class="sxs-lookup"><span data-stu-id="c5420-133">-First</span></span>
<span data-ttu-id="c5420-134">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="c5420-134">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="c5420-135">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="c5420-135">-IdentifierUri</span></span>
<span data-ttu-id="c5420-136">Getirilecek uygulamanın benzersiz tanımlayıcı URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="c5420-136">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="c5420-137">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="c5420-137">-IncludeTotalCount</span></span>
<span data-ttu-id="c5420-138">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="c5420-138">Reports the number of objects in the data set.</span></span> <span data-ttu-id="c5420-139">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="c5420-139">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="c5420-140">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="c5420-140">-ObjectId</span></span>
<span data-ttu-id="c5420-141">Getirilecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="c5420-141">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="c5420-142">-Atla</span><span class="sxs-lookup"><span data-stu-id="c5420-142">-Skip</span></span>
<span data-ttu-id="c5420-143">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="c5420-143">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="c5420-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5420-144">CommonParameters</span></span>
<span data-ttu-id="c5420-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5420-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5420-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5420-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5420-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5420-147">INPUTS</span></span>

### <span data-ttu-id="c5420-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="c5420-148">System.Guid</span></span>

### <span data-ttu-id="c5420-149">System. String</span><span class="sxs-lookup"><span data-stu-id="c5420-149">System.String</span></span>

## <span data-ttu-id="c5420-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5420-150">OUTPUTS</span></span>

### <span data-ttu-id="c5420-151">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c5420-151">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c5420-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5420-152">NOTES</span></span>

## <span data-ttu-id="c5420-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5420-153">RELATED LINKS</span></span>

[<span data-ttu-id="c5420-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c5420-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="c5420-155">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c5420-155">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="c5420-156">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c5420-156">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="c5420-157">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c5420-157">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)



[<span data-ttu-id="c5420-158">Yeni-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="c5420-158">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

