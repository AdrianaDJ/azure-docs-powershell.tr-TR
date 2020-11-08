---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADApplication.md
ms.openlocfilehash: 7f1c1705cfd683766f4e90a383bc39a34209f1e6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933287"
---
# <span data-ttu-id="2e86b-101">Update-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="2e86b-101">Update-AzADApplication</span></span>

## <span data-ttu-id="2e86b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e86b-102">SYNOPSIS</span></span>
<span data-ttu-id="2e86b-103">Var olan bir Azure Active Directory uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e86b-103">Updates an existing azure active directory application.</span></span>

## <span data-ttu-id="2e86b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2e86b-104">SYNTAX</span></span>

### <span data-ttu-id="2e86b-105">ApplicationObjectIdWithUpdateParamsParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2e86b-105">ApplicationObjectIdWithUpdateParamsParameterSet (Default)</span></span>
```
Update-AzADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e86b-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e86b-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -ApplicationId <Guid> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e86b-107">InputObjectWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e86b-107">InputObjectWithUpdateParamsParameterSet</span></span>
```
Update-AzADApplication -InputObject <PSADApplication> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUri <String[]>] [-ReplyUrl <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e86b-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2e86b-108">DESCRIPTION</span></span>
<span data-ttu-id="2e86b-109">Var olan bir Azure Active Directory uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e86b-109">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="2e86b-110">Bu uygulamayla ilişkili kimlik bilgilerini güncelleştirmek için lütfen New-AzADAppCredential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="2e86b-110">To update the credentials associated with this application, please use the New-AzADAppCredential cmdlet.</span></span>

## <span data-ttu-id="2e86b-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2e86b-111">EXAMPLES</span></span>

### <span data-ttu-id="2e86b-112">Örnek 1-uygulamanın görünen adını güncelleyin</span><span class="sxs-lookup"><span data-stu-id="2e86b-112">Example 1 - Update the display name of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName
```

<span data-ttu-id="2e86b-113">Nesne kimliği ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' olan uygulamanın görünen adını ' Yenisdisplayname ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e86b-113">Updates the display name of the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="2e86b-114">Örnek 2-bir uygulamanın tüm özelliklerini güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2e86b-114">Example 2 - Update all properties of an application</span></span>

```
PS C:\> Update-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName MyNewDisplayName -HomePage https://www.microsoft.com -IdentifierUris "https://UpdateAppUri"
```

<span data-ttu-id="2e86b-115">Nesne kimliği ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' olan bir uygulamanın özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="2e86b-115">Updates the properties of an application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7'.</span></span>

### <span data-ttu-id="2e86b-116">Örnek 3-boru kullanarak bir uygulamanın görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="2e86b-116">Example 3 - Update the display name of an application using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 | Update-AzADApplication -DisplayName MyNewDisplayName
```

<span data-ttu-id="2e86b-117">Nesne kimliği ' fb7b3405-ca44-4b5b-8584-12392f5d96d7 ' olan uygulamayı ve uygulamanın görünen adını "Yenisdisplayname" olarak güncelleştirmek için Update-AzADApplication cmdlet 'ine sahip uygulamayı alır.</span><span class="sxs-lookup"><span data-stu-id="2e86b-117">Gets the application with object id 'fb7b3405-ca44-4b5b-8584-12392f5d96d7' and pipes that to the Update-AzADApplication cmdlet to update the display name of the application to "MyNewDisplayName".</span></span>

## <span data-ttu-id="2e86b-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2e86b-118">PARAMETERS</span></span>

### <span data-ttu-id="2e86b-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2e86b-119">-ApplicationId</span></span>
<span data-ttu-id="2e86b-120">Güncelleştirilecek uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="2e86b-120">The application id of the application to update.</span></span>

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

### <span data-ttu-id="2e86b-121">-Availabletootherkiracılar</span><span class="sxs-lookup"><span data-stu-id="2e86b-121">-AvailableToOtherTenants</span></span>
<span data-ttu-id="2e86b-122">Uygulama başka kiralarla paylaşılıyorsa doğru; Aksi takdirde, false.</span><span class="sxs-lookup"><span data-stu-id="2e86b-122">True if the application is shared with other tenants; otherwise, false.</span></span>

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

### <span data-ttu-id="2e86b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e86b-123">-DefaultProfile</span></span>
<span data-ttu-id="2e86b-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2e86b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e86b-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2e86b-125">-DisplayName</span></span>
<span data-ttu-id="2e86b-126">Güncelleştirilecek uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="2e86b-126">The display name for the application to update.</span></span>

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

### <span data-ttu-id="2e86b-127">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="2e86b-127">-HomePage</span></span>
<span data-ttu-id="2e86b-128">Uygulamanın ana sayfasının URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="2e86b-128">The URL to the application's homepage.</span></span>

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

### <span data-ttu-id="2e86b-129">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="2e86b-129">-IdentifierUri</span></span>
<span data-ttu-id="2e86b-130">Uygulamayı tanımlayan URI 'Ler.</span><span class="sxs-lookup"><span data-stu-id="2e86b-130">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="2e86b-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e86b-131">-InputObject</span></span>
<span data-ttu-id="2e86b-132">Güncelleştirilecek uygulamayı temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="2e86b-132">The object representing the application to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: InputObjectWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e86b-133">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="2e86b-133">-ObjectId</span></span>
<span data-ttu-id="2e86b-134">Güncelleştirilecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="2e86b-134">The object id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e86b-135">-ReplyUrl 'Si</span><span class="sxs-lookup"><span data-stu-id="2e86b-135">-ReplyUrl</span></span>
<span data-ttu-id="2e86b-136">Oturum açmak için Kullanıcı belirteçlerinin gönderildiği URL 'Leri veya OAuth 2,0 yetkilendirme kodlarının ve erişim belirteçlerinin gönderildiği yönlendirme URI 'Lerini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2e86b-136">Specifies the URLs that user tokens are sent to for sign in, or the redirect URIs that OAuth 2.0 authorization codes and access tokens are sent to.</span></span>

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

### <span data-ttu-id="2e86b-137">-Onay</span><span class="sxs-lookup"><span data-stu-id="2e86b-137">-Confirm</span></span>
<span data-ttu-id="2e86b-138">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="2e86b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e86b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e86b-139">-WhatIf</span></span>
<span data-ttu-id="2e86b-140">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="2e86b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e86b-141">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="2e86b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e86b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e86b-142">CommonParameters</span></span>
<span data-ttu-id="2e86b-143">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2e86b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e86b-144">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e86b-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e86b-145">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2e86b-145">INPUTS</span></span>

### <span data-ttu-id="2e86b-146">System. String</span><span class="sxs-lookup"><span data-stu-id="2e86b-146">System.String</span></span>

### <span data-ttu-id="2e86b-147">System. Guid</span><span class="sxs-lookup"><span data-stu-id="2e86b-147">System.Guid</span></span>

### <span data-ttu-id="2e86b-148">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="2e86b-148">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="2e86b-149">System. String []</span><span class="sxs-lookup"><span data-stu-id="2e86b-149">System.String[]</span></span>

### <span data-ttu-id="2e86b-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2e86b-150">System.Boolean</span></span>

## <span data-ttu-id="2e86b-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2e86b-151">OUTPUTS</span></span>

### <span data-ttu-id="2e86b-152">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="2e86b-152">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="2e86b-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2e86b-153">NOTES</span></span>

## <span data-ttu-id="2e86b-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2e86b-154">RELATED LINKS</span></span>