---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: bf9f993724de9ed20587a3f4ca136c3531689401
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939233"
---
# <span data-ttu-id="96969-101">Update-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="96969-101">Update-AzureRmADApplication</span></span>

## <span data-ttu-id="96969-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96969-102">SYNOPSIS</span></span>
<span data-ttu-id="96969-103">Var olan bir Azure Active Directory uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="96969-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96969-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="96969-104">SYNTAX</span></span>

### <span data-ttu-id="96969-105">ApplicationObjectIdWithUpdateParamsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="96969-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzureRmADApplication -ObjectId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96969-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="96969-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96969-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="96969-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzureRmADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96969-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="96969-108">DESCRIPTION</span></span>
<span data-ttu-id="96969-109">Var olan bir Azure Active Directory uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="96969-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="96969-110">Bu uygulamayla ilişkili kimlik bilgilerini güncelleştirmek için lütfen New-AzureRmADAppCredential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="96969-110">To update the credentials associated with this application, please use the New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="96969-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="96969-111">EXAMPLES</span></span>

### <span data-ttu-id="96969-112">Örnek 1-uygulamanın görünen adını güncelleyin</span><span class="sxs-lookup"><span data-stu-id="96969-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="96969-113">Nesne kimliği ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' olan uygulamanın görünen adını ' Yenisdisplayname ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="96969-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="96969-114">Örnek 2-bir uygulamanın tüm özelliklerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="96969-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="96969-115">Nesne kimliği ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' olan bir uygulamanın özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="96969-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="96969-116">Örnek 3-boru kullanarak bir uygulamanın görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="96969-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzureRmADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="96969-117">Nesne kimliği ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' olan uygulamayı ve uygulamanın görünen adını "Yenisdisplayname" olarak güncelleştirmek için Update-AzureRmADApplication cmdlet 'ine sahip uygulamayı alır.</span><span class="sxs-lookup"><span data-stu-id="96969-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzureRmADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="96969-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="96969-118">PARAMETERS</span></span>

### <span data-ttu-id="96969-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="96969-119">-ApplicationId</span></span>
<span data-ttu-id="96969-120">Güncelleştirilecek uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="96969-120">The application id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-121">-Availabletootherkiracılar</span><span class="sxs-lookup"><span data-stu-id="96969-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="96969-122">Uygulama başka kiralarla paylaşılıyorsa doğru; Aksi takdirde, false.</span><span class="sxs-lookup"><span data-stu-id="96969-122">True if the application is shared with other tenants; otherwise, false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Boolean
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96969-123">-DefaultProfile</span></span>
<span data-ttu-id="96969-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="96969-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96969-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="96969-125">-DisplayName</span></span>
<span data-ttu-id="96969-126">Güncelleştirilecek uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="96969-126">The display name for the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-127">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="96969-127">-HomePage</span></span>
<span data-ttu-id="96969-128">Uygulamanın ana sayfasının URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="96969-128">The URL to the application's homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-129">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="96969-129">-IdentifierUri</span></span>
<span data-ttu-id="96969-130">Uygulamayı tanımlayan URI 'Ler.</span><span class="sxs-lookup"><span data-stu-id="96969-130">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: IdentifierUris

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96969-131">-InputObject</span></span>
<span data-ttu-id="96969-132">Güncelleştirilecek uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="96969-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-133">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="96969-133">-ObjectId</span></span>
<span data-ttu-id="96969-134">Güncelleştirilecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="96969-134">The object id of the application to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-135">-ReplyUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="96969-135">-ReplyUrl</span></span>
<span data-ttu-id="96969-136">Oturum açmak için Kullanıcı belirteçlerinin gönderildiği URL 'Leri veya OAuth 2,0 yetkilendirme kodlarının ve erişim belirteçlerinin gönderildiği yönlendirme URI 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="96969-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet, ApplicationIdWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases: ReplyUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96969-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="96969-137">-Confirm</span></span>
<span data-ttu-id="96969-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="96969-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96969-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96969-139">-WhatIf</span></span>
<span data-ttu-id="96969-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="96969-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96969-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="96969-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96969-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96969-142">CommonParameters</span></span>
<span data-ttu-id="96969-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="96969-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96969-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96969-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96969-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="96969-145">INPUTS</span></span>

### <span data-ttu-id="96969-146">System. Guid</span><span class="sxs-lookup"><span data-stu-id="96969-146">System.Guid</span></span>

### <span data-ttu-id="96969-147">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="96969-147">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="96969-148">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="96969-148">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="96969-149">System. String</span><span class="sxs-lookup"><span data-stu-id="96969-149">System.String</span></span>

### <span data-ttu-id="96969-150">System. String []</span><span class="sxs-lookup"><span data-stu-id="96969-150">System.String[]</span></span>

### <span data-ttu-id="96969-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="96969-151">System.Boolean</span></span>

## <span data-ttu-id="96969-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="96969-152">OUTPUTS</span></span>

### <span data-ttu-id="96969-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="96969-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="96969-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="96969-154">NOTES</span></span>

## <span data-ttu-id="96969-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="96969-155">RELATED LINKS</span></span>
