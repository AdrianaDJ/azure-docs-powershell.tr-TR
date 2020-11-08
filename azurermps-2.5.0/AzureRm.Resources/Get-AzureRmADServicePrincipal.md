---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 10d95102058c759f9b2641f233bd590364945c71
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939246"
---
# <span data-ttu-id="32865-101">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32865-101">Get-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="32865-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32865-102">SYNOPSIS</span></span>
<span data-ttu-id="32865-103">Active Directory hizmet sorumlularına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="32865-103">Filters active directory service principals.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32865-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32865-104">SYNTAX</span></span>

### <span data-ttu-id="32865-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32865-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32865-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="32865-106">SearchStringParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32865-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="32865-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32865-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="32865-108">ObjectIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32865-109">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="32865-109">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32865-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="32865-110">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="32865-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="32865-111">SPNParameterSet</span></span>
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="32865-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="32865-112">DESCRIPTION</span></span>
<span data-ttu-id="32865-113">Active Directory hizmet sorumlularına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="32865-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="32865-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32865-114">EXAMPLES</span></span>

### <span data-ttu-id="32865-115">Örnek 1-AD hizmeti sorumlularını listeler</span><span class="sxs-lookup"><span data-stu-id="32865-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal
```

<span data-ttu-id="32865-116">Kiracıdaki tüm reklam hizmeti sorumlularını listeler.</span><span class="sxs-lookup"><span data-stu-id="32865-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="32865-117">Örnek 2-sayfalama kullanarak AD hizmeti sorumlularını listeler</span><span class="sxs-lookup"><span data-stu-id="32865-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

<span data-ttu-id="32865-118">Kiracıdaki ilk 100 AD hizmeti sorumlularını listeler.</span><span class="sxs-lookup"><span data-stu-id="32865-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="32865-119">Örnek 3-SPN 'ye göre hizmet sorumlularını Listele</span><span class="sxs-lookup"><span data-stu-id="32865-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="32865-120">SPN ' 36f81fc3-b00f-48cd-8218-3879f51ff39f ' ile hizmet sorumlularını listeler.</span><span class="sxs-lookup"><span data-stu-id="32865-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="32865-121">Örnek 4-arama dizesine göre hizmet sorumlularını Listele</span><span class="sxs-lookup"><span data-stu-id="32865-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="32865-122">Görünen adı "Web" ile başlayan tüm reklam hizmeti sorumlularını listeler.</span><span class="sxs-lookup"><span data-stu-id="32865-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="32865-123">Örnek 5-boru tarafından hizmet sorumlularını listeler</span><span class="sxs-lookup"><span data-stu-id="32865-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

<span data-ttu-id="32865-124">Nesne kimliği ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' olan AD uygulamasını alır ve bu uygulamadaki tüm hizmet sorumlularını listelemek için bunu Get-AzureRmADServicePrincipal cmdlet 'ine alır.</span><span class="sxs-lookup"><span data-stu-id="32865-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzureRmADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="32865-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32865-125">PARAMETERS</span></span>

### <span data-ttu-id="32865-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="32865-126">-ApplicationId</span></span>
<span data-ttu-id="32865-127">Hizmet sorumlusu uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="32865-127">The service principal application id.</span></span>

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

### <span data-ttu-id="32865-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="32865-128">-ApplicationObject</span></span>
<span data-ttu-id="32865-129">Hizmet sorumlusu alınmakta olan uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="32865-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32865-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32865-130">-DefaultProfile</span></span>
<span data-ttu-id="32865-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="32865-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32865-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="32865-132">-DisplayName</span></span>
<span data-ttu-id="32865-133">Hizmet sorumlusu görünen adı.</span><span class="sxs-lookup"><span data-stu-id="32865-133">The service principal display name.</span></span>

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

### <span data-ttu-id="32865-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="32865-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="32865-135">Hizmet sorumlusu arama dizesi.</span><span class="sxs-lookup"><span data-stu-id="32865-135">The service principal search string.</span></span>

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

### <span data-ttu-id="32865-136">-Önce</span><span class="sxs-lookup"><span data-stu-id="32865-136">-First</span></span>
<span data-ttu-id="32865-137">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="32865-137">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="32865-138">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="32865-138">-IncludeTotalCount</span></span>
<span data-ttu-id="32865-139">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="32865-139">Reports the number of objects in the data set.</span></span> <span data-ttu-id="32865-140">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="32865-140">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="32865-141">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="32865-141">-ObjectId</span></span>
<span data-ttu-id="32865-142">Hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="32865-142">Object id of the service principal.</span></span>

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

### <span data-ttu-id="32865-143">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="32865-143">-ServicePrincipalName</span></span>
<span data-ttu-id="32865-144">Hizmetin SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="32865-144">SPN of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32865-145">-Atla</span><span class="sxs-lookup"><span data-stu-id="32865-145">-Skip</span></span>
<span data-ttu-id="32865-146">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="32865-146">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="32865-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32865-147">CommonParameters</span></span>
<span data-ttu-id="32865-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32865-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32865-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32865-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32865-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32865-150">INPUTS</span></span>

### <span data-ttu-id="32865-151">System. String</span><span class="sxs-lookup"><span data-stu-id="32865-151">System.String</span></span>

### <span data-ttu-id="32865-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="32865-152">System.Guid</span></span>

### <span data-ttu-id="32865-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="32865-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="32865-154">Parametreler: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="32865-154">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="32865-155">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32865-155">OUTPUTS</span></span>

### <span data-ttu-id="32865-156">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32865-156">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="32865-157">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32865-157">NOTES</span></span>

## <span data-ttu-id="32865-158">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32865-158">RELATED LINKS</span></span>

[<span data-ttu-id="32865-159">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32865-159">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)



[<span data-ttu-id="32865-160">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="32865-160">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="32865-161">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="32865-161">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="32865-162">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="32865-162">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)
