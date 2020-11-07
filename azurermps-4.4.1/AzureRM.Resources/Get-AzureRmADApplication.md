---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADApplication.md
ms.openlocfilehash: c5276ddbcd10870355f8530c2f04f81122dda382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762695"
---
# <span data-ttu-id="1798a-101">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1798a-101">Get-AzureRmADApplication</span></span>

## <span data-ttu-id="1798a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1798a-102">SYNOPSIS</span></span>
<span data-ttu-id="1798a-103">Var olan Azure Active Directory uygulamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="1798a-103">Lists existing azure active directory applications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1798a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1798a-104">SYNTAX</span></span>

### <span data-ttu-id="1798a-105">EmptyParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="1798a-105">EmptyParameterSet (Default)</span></span>
```
Get-AzureRmADApplication [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1798a-106">Applicationobjectivseçparameterset</span><span class="sxs-lookup"><span data-stu-id="1798a-106">ApplicationObjectIdParameterSet</span></span>
```
Get-AzureRmADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1798a-107">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="1798a-107">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1798a-108">ApplicationDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="1798a-108">ApplicationDisplayNameParameterSet</span></span>
```
Get-AzureRmADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1798a-109">Applicationıdentifieruriparameterset</span><span class="sxs-lookup"><span data-stu-id="1798a-109">ApplicationIdentifierUriParameterSet</span></span>
```
Get-AzureRmADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1798a-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="1798a-110">DESCRIPTION</span></span>
<span data-ttu-id="1798a-111">Var olan Azure Active Directory uygulamalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="1798a-111">Lists existing azure active directory applications.</span></span>
<span data-ttu-id="1798a-112">Uygulama araması objectID, ApplicationId, ıdentifieruri veya DisplayName tarafından yapılabilir.</span><span class="sxs-lookup"><span data-stu-id="1798a-112">Application lookup can be done by ObjectId, ApplicationId, IdentifierUri or DisplayName.</span></span>
<span data-ttu-id="1798a-113">Parametre sağlanmadıysa, kiracı altındaki tüm uygulamaları getirir.</span><span class="sxs-lookup"><span data-stu-id="1798a-113">If no parameter is provided, it fetches all applications under the tenant.</span></span>

## <span data-ttu-id="1798a-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1798a-114">EXAMPLES</span></span>

### <span data-ttu-id="1798a-115">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1798a-115">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication
```

<span data-ttu-id="1798a-116">Kiracı 'nın altındaki tüm uygulamaları listeler.</span><span class="sxs-lookup"><span data-stu-id="1798a-116">Lists all the applications under a tenant.</span></span>

### <span data-ttu-id="1798a-117">--------------------------Örnek 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="1798a-117">--------------------------  Example 2  --------------------------</span></span>
```
PS E:\> Get-AzureRmADApplication -IdentifierUri http://mySecretApp1
```

<span data-ttu-id="1798a-118">URI değerini "" olarak alır http://mySecretApp1 .</span><span class="sxs-lookup"><span data-stu-id="1798a-118">Gets the application with identifier uri as "http://mySecretApp1".</span></span>

## <span data-ttu-id="1798a-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1798a-119">PARAMETERS</span></span>

### <span data-ttu-id="1798a-120">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="1798a-120">-ApplicationId</span></span>
<span data-ttu-id="1798a-121">Getirilecek uygulamanın uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="1798a-121">The application id of the application to fetch.</span></span>

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

### <span data-ttu-id="1798a-122">-DisplayNameStartWith</span><span class="sxs-lookup"><span data-stu-id="1798a-122">-DisplayNameStartWith</span></span>
<span data-ttu-id="1798a-123">Görünen adla başlayan tüm uygulamaları getirir.</span><span class="sxs-lookup"><span data-stu-id="1798a-123">Fetch all applications starting with the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationDisplayNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1798a-124">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="1798a-124">-IdentifierUri</span></span>
<span data-ttu-id="1798a-125">Getirilecek uygulamanın benzersiz tanımlayıcı URI 'Si.</span><span class="sxs-lookup"><span data-stu-id="1798a-125">Unique identifier Uri of the application to fetch.</span></span>

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

### <span data-ttu-id="1798a-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="1798a-126">-ObjectId</span></span>
<span data-ttu-id="1798a-127">Getirilecek uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="1798a-127">The object id of the application to fetch.</span></span>

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

### <span data-ttu-id="1798a-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1798a-128">-DefaultProfile</span></span>
<span data-ttu-id="1798a-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="1798a-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1798a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1798a-130">CommonParameters</span></span>
<span data-ttu-id="1798a-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1798a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1798a-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1798a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1798a-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1798a-133">INPUTS</span></span>

## <span data-ttu-id="1798a-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1798a-134">OUTPUTS</span></span>

### <span data-ttu-id="1798a-135">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication]</span><span class="sxs-lookup"><span data-stu-id="1798a-135">System.Collections.Generic.List\`1[Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication]</span></span>

## <span data-ttu-id="1798a-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1798a-136">NOTES</span></span>

## <span data-ttu-id="1798a-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1798a-137">RELATED LINKS</span></span>

[<span data-ttu-id="1798a-138">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1798a-138">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="1798a-139">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1798a-139">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="1798a-140">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="1798a-140">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="1798a-141">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1798a-141">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="1798a-142">Set-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1798a-142">Set-AzureRmADApplication</span></span>](./Set-AzureRmADApplication.md)

[<span data-ttu-id="1798a-143">Yeni-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="1798a-143">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

