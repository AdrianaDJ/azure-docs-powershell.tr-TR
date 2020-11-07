---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: 6fbbed83f9565a81b305df5cf8b66fd8210c6aec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764779"
---
# <span data-ttu-id="95d7e-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="95d7e-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="95d7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d7e-102">SYNOPSIS</span></span>
<span data-ttu-id="95d7e-103">Var olan bir Azure Active Directory uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="95d7e-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95d7e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="95d7e-104">SYNTAX</span></span>

### <span data-ttu-id="95d7e-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d7e-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d7e-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d7e-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d7e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="95d7e-107">DESCRIPTION</span></span>
<span data-ttu-id="95d7e-108">Var olan bir Azure Active Directory uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="95d7e-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="95d7e-109">Bu uygulamayla ilişkili kimlik bilgilerini güncelleştirmek için lütfen New-AzureRmADAppCredential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="95d7e-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="95d7e-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="95d7e-110">EXAMPLES</span></span>

### <span data-ttu-id="95d7e-111">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="95d7e-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="95d7e-112">ObjectID "fb7b3405-ca44-4b5b-8584-12392f5d96d7" olan bir Azure Active Directory uygulamasının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="95d7e-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="95d7e-113">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="95d7e-113">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="95d7e-114">ObjectID "fb7b3405-ca44-4b5b-8584-12392f5d96d7" bulunan bir Azure Active Directory uygulamasının görünen adını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="95d7e-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="95d7e-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="95d7e-115">PARAMETERS</span></span>

### <span data-ttu-id="95d7e-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="95d7e-116">-ApplicationId</span></span>
<span data-ttu-id="95d7e-117">Güncelleştirilecek uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="95d7e-117">The id of the application to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d7e-118">-Availabletootherkiracılar</span><span class="sxs-lookup"><span data-stu-id="95d7e-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="95d7e-119">Uygulamanın tek kiracılı mı yoksa çoklu kiracı olarak mı güncelleştirileceğini belirten değer.</span><span class="sxs-lookup"><span data-stu-id="95d7e-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d7e-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="95d7e-120">-DisplayName</span></span>
<span data-ttu-id="95d7e-121">Uygulamanın yeni görünen adı.</span><span class="sxs-lookup"><span data-stu-id="95d7e-121">New Display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d7e-122">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="95d7e-122">-HomePage</span></span>
<span data-ttu-id="95d7e-123">Uygulama ana sayfasının yeni URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="95d7e-123">New URL of the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d7e-124">-Identifieruris</span><span class="sxs-lookup"><span data-stu-id="95d7e-124">-IdentifierUris</span></span>
<span data-ttu-id="95d7e-125">Uygulamayı tanımlayan yeni URI 'Ler.</span><span class="sxs-lookup"><span data-stu-id="95d7e-125">New URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d7e-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="95d7e-126">-ObjectId</span></span>
<span data-ttu-id="95d7e-127">Güncelleştirilecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="95d7e-127">The object id of the application to update.</span></span>

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

### <span data-ttu-id="95d7e-128">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="95d7e-128">-ReplyUrls</span></span>
<span data-ttu-id="95d7e-129">Uygulamanın yeni yanıt URL 'leri.</span><span class="sxs-lookup"><span data-stu-id="95d7e-129">New reply urls for the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d7e-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="95d7e-130">-Confirm</span></span>
<span data-ttu-id="95d7e-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="95d7e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d7e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d7e-132">-WhatIf</span></span>
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

### <span data-ttu-id="95d7e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95d7e-133">-DefaultProfile</span></span>
<span data-ttu-id="95d7e-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="95d7e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95d7e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d7e-135">CommonParameters</span></span>
<span data-ttu-id="95d7e-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="95d7e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d7e-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d7e-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d7e-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="95d7e-138">INPUTS</span></span>

## <span data-ttu-id="95d7e-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="95d7e-139">OUTPUTS</span></span>

### <span data-ttu-id="95d7e-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="95d7e-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="95d7e-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="95d7e-141">NOTES</span></span>

## <span data-ttu-id="95d7e-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="95d7e-142">RELATED LINKS</span></span>

[<span data-ttu-id="95d7e-143">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="95d7e-143">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="95d7e-144">Yeni-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="95d7e-144">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="95d7e-145">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="95d7e-145">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="95d7e-146">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="95d7e-146">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="95d7e-147">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="95d7e-147">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="95d7e-148">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="95d7e-148">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

