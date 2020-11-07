---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADServicePrincipal.md
ms.openlocfilehash: 0dc49732a6e6ad614a0330c3fe24b412be898a54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759452"
---
# <span data-ttu-id="16982-101">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="16982-101">Get-AzADServicePrincipal</span></span>

## <span data-ttu-id="16982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16982-102">SYNOPSIS</span></span>
<span data-ttu-id="16982-103">Active Directory hizmet sorumlularına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="16982-103">Filters active directory service principals.</span></span>

## <span data-ttu-id="16982-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16982-104">SYNTAX</span></span>

### <span data-ttu-id="16982-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="16982-105">EmptyParameterSet (Default)</span></span>
```
Get-AzADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="16982-106">SearchStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="16982-106">SearchStringParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="16982-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="16982-107">DisplayNameParameterSet</span></span>
```
Get-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="16982-108">NesneKimliği</span><span class="sxs-lookup"><span data-stu-id="16982-108">ObjectIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="16982-109">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="16982-109">ApplicationIdParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="16982-110">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="16982-110">ApplicationObjectParameterSet</span></span>
```
Get-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="16982-111">SPNParameterSet</span><span class="sxs-lookup"><span data-stu-id="16982-111">SPNParameterSet</span></span>
```
Get-AzADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="16982-112">Tanım</span><span class="sxs-lookup"><span data-stu-id="16982-112">DESCRIPTION</span></span>
<span data-ttu-id="16982-113">Active Directory hizmet sorumlularına filtre uygular.</span><span class="sxs-lookup"><span data-stu-id="16982-113">Filters active directory service principals.</span></span>

## <span data-ttu-id="16982-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16982-114">EXAMPLES</span></span>

### <span data-ttu-id="16982-115">Örnek 1-AD hizmeti sorumlularını listeler</span><span class="sxs-lookup"><span data-stu-id="16982-115">Example 1 - List AD service principals</span></span>

```
PS C:\> Get-AzADServicePrincipal
```

<span data-ttu-id="16982-116">Kiracıdaki tüm reklam hizmeti sorumlularını listeler.</span><span class="sxs-lookup"><span data-stu-id="16982-116">Lists all AD service principals in a tenant.</span></span>

### <span data-ttu-id="16982-117">Örnek 2-sayfalama kullanarak AD hizmeti sorumlularını listeler</span><span class="sxs-lookup"><span data-stu-id="16982-117">Example 2 - List AD service principals using paging</span></span>

```
PS C:\> Get-AzADServicePrincipal -First 100
```

<span data-ttu-id="16982-118">Kiracıdaki ilk 100 AD hizmeti sorumlularını listeler.</span><span class="sxs-lookup"><span data-stu-id="16982-118">Lists the first 100 AD service principals in a tenant.</span></span>

### <span data-ttu-id="16982-119">Örnek 3-SPN 'ye göre hizmet sorumlularını Listele</span><span class="sxs-lookup"><span data-stu-id="16982-119">Example 3 - List service principals by SPN</span></span>

```
PS C:\> Get-AzADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

<span data-ttu-id="16982-120">SPN ' 36f81fc3-b00f-48cd-8218-3879f51ff39f ' ile hizmet sorumlularını listeler.</span><span class="sxs-lookup"><span data-stu-id="16982-120">Lists service principals with the SPN '36f81fc3-b00f-48cd-8218-3879f51ff39f'.</span></span>

### <span data-ttu-id="16982-121">Örnek 4-arama dizesine göre hizmet sorumlularını Listele</span><span class="sxs-lookup"><span data-stu-id="16982-121">Example 4 - List service principals by search string</span></span>

```
PS C:\> Get-AzADServicePrincipal -SearchString "Web"
```

<span data-ttu-id="16982-122">Görünen adı "Web" ile başlayan tüm reklam hizmeti sorumlularını listeler.</span><span class="sxs-lookup"><span data-stu-id="16982-122">Lists all AD service principals whose display name start with "Web".</span></span>

### <span data-ttu-id="16982-123">Örnek 5-boru tarafından hizmet sorumlularını listeler</span><span class="sxs-lookup"><span data-stu-id="16982-123">Example 5 - List service principals by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzADServicePrincipal
```

<span data-ttu-id="16982-124">Nesne kimliği ' 39e64ec6-569b-4030-8e1c-c3c519a05d69 ' olan AD uygulamasını alır ve bu uygulamadaki tüm hizmet sorumlularını listelemek için bunu Get-AzADServicePrincipal cmdlet 'ine alır.</span><span class="sxs-lookup"><span data-stu-id="16982-124">Gets the AD application with object id '39e64ec6-569b-4030-8e1c-c3c519a05d69' and pipes it to the Get-AzADServicePrincipal cmdlet to list all service principals for that application.</span></span>

## <span data-ttu-id="16982-125">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16982-125">PARAMETERS</span></span>

### <span data-ttu-id="16982-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="16982-126">-ApplicationId</span></span>
<span data-ttu-id="16982-127">Hizmet sorumlusu uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="16982-127">The service principal application id.</span></span>

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

### <span data-ttu-id="16982-128">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="16982-128">-ApplicationObject</span></span>
<span data-ttu-id="16982-129">Hizmet sorumlusu alınmakta olan uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="16982-129">The application object whose service principal is being retrieved.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16982-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16982-130">-DefaultProfile</span></span>
<span data-ttu-id="16982-131">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16982-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16982-132">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="16982-132">-DisplayName</span></span>
<span data-ttu-id="16982-133">Hizmet sorumlusu görünen adı.</span><span class="sxs-lookup"><span data-stu-id="16982-133">The service principal display name.</span></span>

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

### <span data-ttu-id="16982-134">-DisplayNameBeginsWith</span><span class="sxs-lookup"><span data-stu-id="16982-134">-DisplayNameBeginsWith</span></span>
<span data-ttu-id="16982-135">Hizmet sorumlusu arama dizesi.</span><span class="sxs-lookup"><span data-stu-id="16982-135">The service principal search string.</span></span>

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

### <span data-ttu-id="16982-136">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="16982-136">-ObjectId</span></span>
<span data-ttu-id="16982-137">Hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="16982-137">Object id of the service principal.</span></span>

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

### <span data-ttu-id="16982-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="16982-138">-ServicePrincipalName</span></span>
<span data-ttu-id="16982-139">Hizmetin SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="16982-139">SPN of the service.</span></span>

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

### <span data-ttu-id="16982-140">-Includetoplamsayısı</span><span class="sxs-lookup"><span data-stu-id="16982-140">-IncludeTotalCount</span></span>
<span data-ttu-id="16982-141">Veri kümesindeki nesnelerin sayısını raporlar.</span><span class="sxs-lookup"><span data-stu-id="16982-141">Reports the number of objects in the data set.</span></span> <span data-ttu-id="16982-142">Şu anda bu parametre hiçbir şey yapmaz.</span><span class="sxs-lookup"><span data-stu-id="16982-142">Currently, this parameter does nothing.</span></span>

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

### <span data-ttu-id="16982-143">-Atla</span><span class="sxs-lookup"><span data-stu-id="16982-143">-Skip</span></span>
<span data-ttu-id="16982-144">İlk N nesneyi yoksayar ve kalan nesneleri alır.</span><span class="sxs-lookup"><span data-stu-id="16982-144">Ignores the first N objects and then gets the remaining objects.</span></span>

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

### <span data-ttu-id="16982-145">-Önce</span><span class="sxs-lookup"><span data-stu-id="16982-145">-First</span></span>
<span data-ttu-id="16982-146">Döndürülecek en fazla nesne sayısı.</span><span class="sxs-lookup"><span data-stu-id="16982-146">The maximum number of objects to return.</span></span>

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

### <span data-ttu-id="16982-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16982-147">CommonParameters</span></span>
<span data-ttu-id="16982-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16982-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16982-149">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16982-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16982-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16982-150">INPUTS</span></span>

### <span data-ttu-id="16982-151">System. String</span><span class="sxs-lookup"><span data-stu-id="16982-151">System.String</span></span>

### <span data-ttu-id="16982-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="16982-152">System.Guid</span></span>

### <span data-ttu-id="16982-153">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="16982-153">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="16982-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16982-154">OUTPUTS</span></span>

### <span data-ttu-id="16982-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="16982-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="16982-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16982-156">NOTES</span></span>

## <span data-ttu-id="16982-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16982-157">RELATED LINKS</span></span>

[<span data-ttu-id="16982-158">Yeni-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="16982-158">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="16982-159">Set-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="16982-159">Set-AzADServicePrincipal</span></span>](./Set-AzADServicePrincipal.md)

[<span data-ttu-id="16982-160">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="16982-160">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="16982-161">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="16982-161">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="16982-162">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="16982-162">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

