---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA97DB6F-F64D-417E-BD72-C2EBB2EC1AA4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADApplication.md
ms.openlocfilehash: a8c1aa2d0f22a9c6dc6260384e51140cb930106a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593434"
---
# <span data-ttu-id="6661d-101">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="6661d-101">Set-AzureRmADApplication</span></span>

## <span data-ttu-id="6661d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6661d-102">SYNOPSIS</span></span>
<span data-ttu-id="6661d-103">Var olan bir Azure Active Directory uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6661d-103">Updates an existing azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6661d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6661d-104">SYNTAX</span></span>

### <span data-ttu-id="6661d-105">ApplicationObjectIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6661d-105">ApplicationObjectIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ObjectId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6661d-106">ApplicationIdWithUpdateParamsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6661d-106">ApplicationIdWithUpdateParamsParameterSet</span></span>
```
Set-AzureRmADApplication -ApplicationId <String> [-DisplayName <String>] [-HomePage <String>]
 [-IdentifierUris <String[]>] [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6661d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6661d-107">DESCRIPTION</span></span>
<span data-ttu-id="6661d-108">Var olan bir Azure Active Directory uygulamasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6661d-108">Updates an existing azure active directory application.</span></span>
<span data-ttu-id="6661d-109">Bu uygulamayla ilişkili kimlik bilgilerini güncelleştirmek için lütfen New-AzureRmADAppCredential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="6661d-109">To update the credentials associated with this application, please use New-AzureRmADAppCredential cmdlet.</span></span>

## <span data-ttu-id="6661d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6661d-110">EXAMPLES</span></span>

### <span data-ttu-id="6661d-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6661d-111">Example 1</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName" -HomePage "https://www.microsoft.com" -IdentifierUris "http://UpdatedApp" -AvailableToOtherTenants $false
```

<span data-ttu-id="6661d-112">ObjectID "fb7b3405-ca44-4b5b-8584-12392f5d96d7" olan bir Azure Active Directory uygulamasının özelliklerini güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6661d-112">Updates the properties of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

### <span data-ttu-id="6661d-113">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="6661d-113">Example 2</span></span>
```
PS E:\> Set-AzureRmADApplication -ObjectId fb7b3405-ca44-4b5b-8584-12392f5d96d7 -DisplayName "UpdatedAppName"
```

<span data-ttu-id="6661d-114">ObjectID "fb7b3405-ca44-4b5b-8584-12392f5d96d7" bulunan bir Azure Active Directory uygulamasının görünen adını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6661d-114">Updates the display name of an existing azure active directory application with objectId "fb7b3405-ca44-4b5b-8584-12392f5d96d7".</span></span>

## <span data-ttu-id="6661d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6661d-115">PARAMETERS</span></span>

### <span data-ttu-id="6661d-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="6661d-116">-ApplicationId</span></span>
<span data-ttu-id="6661d-117">Güncelleştirilecek uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="6661d-117">The id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-118">-Availabletootherkiracılar</span><span class="sxs-lookup"><span data-stu-id="6661d-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="6661d-119">Uygulamanın tek kiracılı mı yoksa çoklu kiracı olarak mı güncelleştirileceğini belirten değer.</span><span class="sxs-lookup"><span data-stu-id="6661d-119">The value specifying whether the application is updated to be a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6661d-120">-DefaultProfile</span></span>
<span data-ttu-id="6661d-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="6661d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6661d-122">-DisplayName</span></span>
<span data-ttu-id="6661d-123">Uygulamanın yeni görünen adı.</span><span class="sxs-lookup"><span data-stu-id="6661d-123">New Display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-124">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="6661d-124">-HomePage</span></span>
<span data-ttu-id="6661d-125">Uygulama ana sayfasının yeni URL 'SI.</span><span class="sxs-lookup"><span data-stu-id="6661d-125">New URL of the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-126">-Identifieruris</span><span class="sxs-lookup"><span data-stu-id="6661d-126">-IdentifierUris</span></span>
<span data-ttu-id="6661d-127">Uygulamayı tanımlayan yeni URI 'Ler.</span><span class="sxs-lookup"><span data-stu-id="6661d-127">New URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-128">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="6661d-128">-ObjectId</span></span>
<span data-ttu-id="6661d-129">Güncelleştirilecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="6661d-129">The object id of the application to update.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithUpdateParamsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-130">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="6661d-130">-ReplyUrls</span></span>
<span data-ttu-id="6661d-131">Uygulamanın yeni yanıt URL 'leri.</span><span class="sxs-lookup"><span data-stu-id="6661d-131">New reply urls for the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="6661d-132">-Confirm</span></span>
<span data-ttu-id="6661d-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6661d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6661d-134">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6661d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6661d-135">CommonParameters</span></span>
<span data-ttu-id="6661d-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6661d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6661d-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6661d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6661d-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6661d-138">INPUTS</span></span>

### <span data-ttu-id="6661d-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="6661d-139">None</span></span>
<span data-ttu-id="6661d-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="6661d-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6661d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6661d-141">OUTPUTS</span></span>

### <span data-ttu-id="6661d-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="6661d-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="6661d-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6661d-143">NOTES</span></span>

## <span data-ttu-id="6661d-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6661d-144">RELATED LINKS</span></span>

[<span data-ttu-id="6661d-145">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="6661d-145">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="6661d-146">Yeni-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="6661d-146">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="6661d-147">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="6661d-147">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="6661d-148">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6661d-148">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="6661d-149">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6661d-149">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="6661d-150">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="6661d-150">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

