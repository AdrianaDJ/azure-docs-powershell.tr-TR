---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: 7bfa908e83d7731ca2ed5613d82f42b19c392b2f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267653"
---
# <span data-ttu-id="8520d-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8520d-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="8520d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8520d-102">SYNOPSIS</span></span>
<span data-ttu-id="8520d-103">Uygulamayla ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="8520d-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="8520d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8520d-104">SYNTAX</span></span>

### <span data-ttu-id="8520d-105">Applicationobjectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="8520d-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8520d-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="8520d-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8520d-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8520d-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8520d-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8520d-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8520d-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="8520d-109">DESCRIPTION</span></span>
<span data-ttu-id="8520d-110">Bir uygulamayla ilişkili kimlik bilgilerinin listesini almak için Get-AzADAppCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="8520d-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="8520d-111">Bu komut, uygulamayla ilişkili tüm kimlik bilgileri (kimlik bilgileri değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="8520d-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="8520d-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8520d-112">EXAMPLES</span></span>

### <span data-ttu-id="8520d-113">Örnek 1: nesne kimliğine göre uygulama kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="8520d-113">Example 1: Get application credentials by object id</span></span>

```powershell
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="8520d-114">Nesne kimliği ' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' olan uygulamayla ilişkili kimlik bilgileri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="8520d-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="8520d-115">Örnek 2: boru ile uygulama kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="8520d-115">Example 2: Get application credentials by piping</span></span>

```powershell
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="8520d-116">Uygulama kimliği ' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' ile uygulamayı alır Get-AzADAppCredential ve bu uygulamanın tüm kimlik bilgilerini listeme</span><span class="sxs-lookup"><span data-stu-id="8520d-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="8520d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8520d-117">PARAMETERS</span></span>

### <span data-ttu-id="8520d-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="8520d-118">-ApplicationId</span></span>
<span data-ttu-id="8520d-119">Kimlik bilgilerinin alınacağı uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="8520d-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="8520d-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="8520d-120">-ApplicationObject</span></span>
<span data-ttu-id="8520d-121">Kimlik bilgilerini alacak uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="8520d-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="8520d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8520d-122">-DefaultProfile</span></span>
<span data-ttu-id="8520d-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8520d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8520d-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8520d-124">-DisplayName</span></span>
<span data-ttu-id="8520d-125">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="8520d-125">The display name of the application.</span></span>

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

### <span data-ttu-id="8520d-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="8520d-126">-ObjectId</span></span>
<span data-ttu-id="8520d-127">Kimlik bilgilerinin alınacağı uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="8520d-127">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8520d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8520d-128">CommonParameters</span></span>
<span data-ttu-id="8520d-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8520d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8520d-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8520d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8520d-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8520d-131">INPUTS</span></span>

### <span data-ttu-id="8520d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8520d-132">System.String</span></span>

### <span data-ttu-id="8520d-133">System. Guid</span><span class="sxs-lookup"><span data-stu-id="8520d-133">System.Guid</span></span>

### <span data-ttu-id="8520d-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8520d-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8520d-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8520d-135">OUTPUTS</span></span>

### <span data-ttu-id="8520d-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="8520d-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="8520d-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8520d-137">NOTES</span></span>

## <span data-ttu-id="8520d-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8520d-138">RELATED LINKS</span></span>

[<span data-ttu-id="8520d-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8520d-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="8520d-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8520d-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="8520d-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8520d-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

