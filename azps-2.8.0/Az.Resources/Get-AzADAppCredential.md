---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzADAppCredential.md
ms.openlocfilehash: fdef07255316b1d7529202c36b844e8732c76390
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93932612"
---
# <span data-ttu-id="ee941-101">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ee941-101">Get-AzADAppCredential</span></span>

## <span data-ttu-id="ee941-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee941-102">SYNOPSIS</span></span>
<span data-ttu-id="ee941-103">Uygulamayla ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="ee941-103">Retrieves a list of credentials associated with an application.</span></span>

## <span data-ttu-id="ee941-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ee941-104">SYNTAX</span></span>

### <span data-ttu-id="ee941-105">Applicationobjectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ee941-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee941-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="ee941-106">ApplicationIdParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee941-107">DisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee941-107">DisplayNameParameterSet</span></span>
```
Get-AzADAppCredential -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ee941-108">ApplicationObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee941-108">ApplicationObjectParameterSet</span></span>
```
Get-AzADAppCredential -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ee941-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="ee941-109">DESCRIPTION</span></span>
<span data-ttu-id="ee941-110">Bir uygulamayla ilişkili kimlik bilgilerinin listesini almak için Get-AzADAppCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="ee941-110">The Get-AzADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>
<span data-ttu-id="ee941-111">Bu komut, uygulamayla ilişkili tüm kimlik bilgileri (kimlik bilgileri değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="ee941-111">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="ee941-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ee941-112">EXAMPLES</span></span>

### <span data-ttu-id="ee941-113">Örnek 1-nesne kimliğine göre uygulama kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="ee941-113">Example 1 - Get application credentials by object id</span></span>

```
PS C:\> Get-AzADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="ee941-114">Nesne kimliği ' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' olan uygulamayla ilişkili kimlik bilgileri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="ee941-114">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="ee941-115">Örnek 2-boru ile uygulama kimlik bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="ee941-115">Example 2 - Get application credentials by piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | Get-AzADAppCredential
```

<span data-ttu-id="ee941-116">Uygulama kimliği ' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' ile uygulamayı alır Get-AzADAppCredential ve bu uygulamanın tüm kimlik bilgilerini listeme</span><span class="sxs-lookup"><span data-stu-id="ee941-116">Gets the application with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes it to the Get-AzADAppCredential cmdlet to list all of the credentials for that application.</span></span>

## <span data-ttu-id="ee941-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ee941-117">PARAMETERS</span></span>

### <span data-ttu-id="ee941-118">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ee941-118">-ApplicationId</span></span>
<span data-ttu-id="ee941-119">Kimlik bilgilerinin alınacağı uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="ee941-119">The id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="ee941-120">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="ee941-120">-ApplicationObject</span></span>
<span data-ttu-id="ee941-121">Kimlik bilgilerini alacak uygulama nesnesi.</span><span class="sxs-lookup"><span data-stu-id="ee941-121">The application object to retrieve credentials from.</span></span>

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

### <span data-ttu-id="ee941-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee941-122">-DefaultProfile</span></span>
<span data-ttu-id="ee941-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ee941-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee941-124">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ee941-124">-DisplayName</span></span>
<span data-ttu-id="ee941-125">Uygulamanın görünen adı.</span><span class="sxs-lookup"><span data-stu-id="ee941-125">The display name of the application.</span></span>

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

### <span data-ttu-id="ee941-126">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="ee941-126">-ObjectId</span></span>
<span data-ttu-id="ee941-127">Kimlik bilgilerinin alınacağı uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="ee941-127">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="ee941-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee941-128">CommonParameters</span></span>
<span data-ttu-id="ee941-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ee941-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee941-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee941-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee941-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ee941-131">INPUTS</span></span>

### <span data-ttu-id="ee941-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ee941-132">System.String</span></span>

### <span data-ttu-id="ee941-133">System. Guid</span><span class="sxs-lookup"><span data-stu-id="ee941-133">System.Guid</span></span>

### <span data-ttu-id="ee941-134">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ee941-134">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="ee941-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ee941-135">OUTPUTS</span></span>

### <span data-ttu-id="ee941-136">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="ee941-136">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="ee941-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ee941-137">NOTES</span></span>

## <span data-ttu-id="ee941-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ee941-138">RELATED LINKS</span></span>

[<span data-ttu-id="ee941-139">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ee941-139">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="ee941-140">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ee941-140">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="ee941-141">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="ee941-141">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

