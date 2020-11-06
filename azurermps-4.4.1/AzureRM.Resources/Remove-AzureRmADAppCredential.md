---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: C61FA834-BEBE-4DBF-888F-C6CB8CC95390
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmADAppCredential.md
ms.openlocfilehash: a5e99f045701a373e14990c25627696d40a04a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592560"
---
# <span data-ttu-id="cdb8e-101">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cdb8e-101">Remove-AzureRmADAppCredential</span></span>

## <span data-ttu-id="cdb8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdb8e-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb8e-103">Uygulamadaki kimlik bilgilerini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-103">Removes a credential from an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cdb8e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cdb8e-104">SYNTAX</span></span>

### <span data-ttu-id="cdb8e-105">Applicationobjectivseçwithkeyidparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="cdb8e-105">ApplicationObjectIdWithKeyIdParameterSet (Default)</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb8e-106">Applicationobjectivseçwithallparameterset</span><span class="sxs-lookup"><span data-stu-id="cdb8e-106">ApplicationObjectIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ObjectId <String> [-All] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb8e-107">Applicationıdwithkeyıdparameterset</span><span class="sxs-lookup"><span data-stu-id="cdb8e-107">ApplicationIdWithKeyIdParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> -KeyId <Guid> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb8e-108">Applicationıdwithallparameterset</span><span class="sxs-lookup"><span data-stu-id="cdb8e-108">ApplicationIdWithAllParameterSet</span></span>
```
Remove-AzureRmADAppCredential -ApplicationId <String> [-All] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb8e-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="cdb8e-109">DESCRIPTION</span></span>
<span data-ttu-id="cdb8e-110">Remove-AzureRmADAppCredential cmdlet 'i, tehlikeye karşı veya kimlik bilgisi anahtarı geçişi süre sonunun bir parçası olarak bir uygulamadan kimlik bilgileri kaldırmak için kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-110">The Remove-AzureRmADAppCredential cmdlet can be used to remove a credential key from an application in the case of a compromise or as part of credential key rollover expiration.</span></span>
<span data-ttu-id="cdb8e-111">Uygulama, nesne KIMLIĞI veya AppID sağlayarak tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-111">The application is identified by supplying either the object ID or AppId.</span></span>
<span data-ttu-id="cdb8e-112">Kaldırılacak kimlik bilgileri, tek bir kimlik bilgisinin kaldırılması veya ' tümü ' anahtarıyla uygulamayla ilişkili tüm kimlik bilgilerinin silinmesi durumunda anahtar KIMLIĞIYLE tanımlanır.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-112">The credential to be removed is identified by its key ID if an individual credential is to be removed or with an 'All' switch to delete all credentials associated with the application.</span></span>

## <span data-ttu-id="cdb8e-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cdb8e-113">EXAMPLES</span></span>

### <span data-ttu-id="cdb8e-114">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cdb8e-114">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ObjectId 7663d3fb-6f86-4352-9e6d-cf9d50d5ee82 -KeyId 9044423a-60a3-45ac-9ab1-09534157ebb
```

<span data-ttu-id="cdb8e-115">Bu komut bir uygulamadan kimlik bilgileri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-115">This command removes a credential key from an application.</span></span>
<span data-ttu-id="cdb8e-116">Bu örnekte, "9044423a-60a3-45ac-9ab1-09534157ebb" kimlikli anahtar uygulamadan kaldırılır.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-116">In this example, the key with Id "9044423a-60a3-45ac-9ab1-09534157ebb" will be removed from the application.</span></span>

### <span data-ttu-id="cdb8e-117">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cdb8e-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Remove-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -All
```

<span data-ttu-id="cdb8e-118">Bu komut bir uygulamadan kimlik bilgileri kaldırır.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-118">This command removes a credential key from an application.</span></span>
<span data-ttu-id="cdb8e-119">Bu örnekte, tüm kimlik bilgileri, ApplicationId "4589cd6b-3d79-4bb4-/2</span><span class="sxs-lookup"><span data-stu-id="cdb8e-119">In this example, all credentials will be removed from the application associated with the applicationId "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span></span>

## <span data-ttu-id="cdb8e-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cdb8e-120">PARAMETERS</span></span>

### <span data-ttu-id="cdb8e-121">-Tümü</span><span class="sxs-lookup"><span data-stu-id="cdb8e-121">-All</span></span>
<span data-ttu-id="cdb8e-122">Uygulamayla ilişkili tüm kimlik bilgilerini kaldırmak için geçiş yapın.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-122">Switch to remove all the credentials associated with the application.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ApplicationObjectIdWithAllParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb8e-123">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cdb8e-123">-ApplicationId</span></span>
<span data-ttu-id="cdb8e-124">Kimlik bilgilerinin kaldırılacağı uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-124">The id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithKeyIdParameterSet, ApplicationIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb8e-125">-Force</span><span class="sxs-lookup"><span data-stu-id="cdb8e-125">-Force</span></span>
<span data-ttu-id="cdb8e-126">Onay yapmadan kimlik bilgisini silmeye geçin.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-126">Switch to delete credential without a confirmation.</span></span>

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

### <span data-ttu-id="cdb8e-127">-KeyId</span><span class="sxs-lookup"><span data-stu-id="cdb8e-127">-KeyId</span></span>
<span data-ttu-id="cdb8e-128">Kaldırılacak kimlik bilgileri anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-128">Specifies the credential key to be removed.</span></span>
<span data-ttu-id="cdb8e-129">Uygulamanın anahtar kimlikleri, Get-AzureRmADAppCredential cmdlet 'i kullanılarak elde edilebilir.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-129">The key Ids for the application can be obtained using the Get-AzureRmADAppCredential cmdlet.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationIdWithKeyIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb8e-130">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="cdb8e-130">-ObjectId</span></span>
<span data-ttu-id="cdb8e-131">Kimlik bilgilerinin kaldırılacağı uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-131">The object id of the application to remove the credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithKeyIdParameterSet, ApplicationObjectIdWithAllParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cdb8e-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="cdb8e-132">-Confirm</span></span>
<span data-ttu-id="cdb8e-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb8e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb8e-134">-WhatIf</span></span>
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

### <span data-ttu-id="cdb8e-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb8e-135">-DefaultProfile</span></span>
<span data-ttu-id="cdb8e-136">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cdb8e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb8e-137">CommonParameters</span></span>
<span data-ttu-id="cdb8e-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cdb8e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb8e-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdb8e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb8e-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cdb8e-140">INPUTS</span></span>

## <span data-ttu-id="cdb8e-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cdb8e-141">OUTPUTS</span></span>

## <span data-ttu-id="cdb8e-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cdb8e-142">NOTES</span></span>

## <span data-ttu-id="cdb8e-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cdb8e-143">RELATED LINKS</span></span>

[<span data-ttu-id="cdb8e-144">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cdb8e-144">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="cdb8e-145">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cdb8e-145">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="cdb8e-146">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cdb8e-146">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
