---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
ms.openlocfilehash: 5390cf033174f473a08a8407028a709a02677352
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939252"
---
# <span data-ttu-id="2c485-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2c485-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="2c485-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c485-102">SYNOPSIS</span></span>
<span data-ttu-id="2c485-103">Uygulamayla ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="2c485-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c485-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2c485-104">SYNTAX</span></span>

### <span data-ttu-id="2c485-105">Applicationobjectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2c485-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2c485-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="2c485-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c485-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c485-107">DisplayNameParameterSet</span></span>
```
Get-AzureRmADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c485-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c485-108">ApplicationObjectParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c485-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="2c485-109">DESCRIPTION</span></span>
<span data-ttu-id="2c485-110">Bir uygulamayla ilişkili kimlik bilgilerinin listesini almak için Get-AzureRmADAppCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="2c485-110">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="2c485-111">Bu komut, uygulamayla ilişkili tüm kimlik bilgileri (kimlik bilgileri değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="2c485-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="2c485-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2c485-112">EXAMPLES</span></span>

### <span data-ttu-id="2c485-113">Örnek 1-nesne kimliğine göre uygulama kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="2c485-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="2c485-114">Nesne kimliği ' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' olan uygulamayla ilişkili kimlik bilgileri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="2c485-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="2c485-115">Örnek 2-boru ile uygulama kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="2c485-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzureRmADAppCredential
```

<span data-ttu-id="2c485-116">Uygulama kimliği ' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' ile uygulamayı alır Get-AzureRmADAppCredential ve bu uygulamanın tüm kimlik bilgilerini listeme</span><span class="sxs-lookup"><span data-stu-id="2c485-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzureRmADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="2c485-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2c485-117">PARAMETERS</span></span>

### <span data-ttu-id="2c485-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2c485-118">-ApplicationId</span></span>
<span data-ttu-id="2c485-119">Kimlik bilgilerinin alınacağı uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="2c485-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="2c485-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="2c485-120">-ApplicationObject</span></span>
<span data-ttu-id="2c485-121">Kimlik bilgilerini alacak uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2c485-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="2c485-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c485-122">-DefaultProfile</span></span>
<span data-ttu-id="2c485-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2c485-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2c485-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2c485-124">-DisplayName</span></span>
<span data-ttu-id="2c485-125">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="2c485-125">The display name of the application.</span></span>

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

### <span data-ttu-id="2c485-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="2c485-126">-ObjectId</span></span>
<span data-ttu-id="2c485-127">Kimlik bilgilerinin alınacağı uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="2c485-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="2c485-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c485-128">CommonParameters</span></span>
<span data-ttu-id="2c485-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2c485-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c485-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c485-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c485-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2c485-131">INPUTS</span></span>

### <span data-ttu-id="2c485-132">System. Guid</span><span class="sxs-lookup"><span data-stu-id="2c485-132">System.Guid</span></span>

### <span data-ttu-id="2c485-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2c485-133">System.String</span></span>

### <span data-ttu-id="2c485-134">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="2c485-134">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="2c485-135">Parametreler: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2c485-135">Parameters: ApplicationObject (ByValue)</span></span>

## <span data-ttu-id="2c485-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2c485-136">OUTPUTS</span></span>

### <span data-ttu-id="2c485-137">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="2c485-137">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="2c485-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2c485-138">NOTES</span></span>

## <span data-ttu-id="2c485-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2c485-139">RELATED LINKS</span></span>

[<span data-ttu-id="2c485-140">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2c485-140">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="2c485-141">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2c485-141">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="2c485-142">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2c485-142">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
