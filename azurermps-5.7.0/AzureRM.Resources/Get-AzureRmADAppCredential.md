---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: fa2368e1982e66d8edecc465d1f6ded3a3d75205
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589692"
---
# <span data-ttu-id="e6fa0-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e6fa0-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="e6fa0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e6fa0-102">SYNOPSIS</span></span>
<span data-ttu-id="e6fa0-103">Uygulamayla ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="e6fa0-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6fa0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e6fa0-104">SYNTAX</span></span>

### <span data-ttu-id="e6fa0-105">Applicationobjectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e6fa0-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6fa0-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e6fa0-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e6fa0-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e6fa0-107">DESCRIPTION</span></span>
<span data-ttu-id="e6fa0-108">Bir uygulamayla ilişkili kimlik bilgilerinin listesini almak için Get-AzureRmADAppCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="e6fa0-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="e6fa0-109">Bu komut, uygulamayla ilişkili tüm kimlik bilgileri (kimlik bilgileri değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="e6fa0-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="e6fa0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e6fa0-110">EXAMPLES</span></span>

### <span data-ttu-id="e6fa0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="e6fa0-111">Example 1</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="e6fa0-112">Nesne kimliği ' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' olan uygulamayla ilişkili kimlik bilgileri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="e6fa0-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="e6fa0-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e6fa0-113">PARAMETERS</span></span>

### <span data-ttu-id="e6fa0-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e6fa0-114">-ApplicationId</span></span>
<span data-ttu-id="e6fa0-115">Kimlik bilgilerinin alınacağı uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="e6fa0-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fa0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6fa0-116">-DefaultProfile</span></span>
<span data-ttu-id="e6fa0-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="e6fa0-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6fa0-118">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="e6fa0-118">-ObjectId</span></span>
<span data-ttu-id="e6fa0-119">Kimlik bilgilerinin alınacağı uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="e6fa0-119">The object id of the application to retrieve credentials from.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6fa0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6fa0-120">CommonParameters</span></span>
<span data-ttu-id="e6fa0-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e6fa0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6fa0-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6fa0-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6fa0-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e6fa0-123">INPUTS</span></span>

### <span data-ttu-id="e6fa0-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e6fa0-124">None</span></span>
<span data-ttu-id="e6fa0-125">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="e6fa0-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6fa0-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e6fa0-126">OUTPUTS</span></span>

### <span data-ttu-id="e6fa0-127">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="e6fa0-127">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e6fa0-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e6fa0-128">NOTES</span></span>

## <span data-ttu-id="e6fa0-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e6fa0-129">RELATED LINKS</span></span>

[<span data-ttu-id="e6fa0-130">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e6fa0-130">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="e6fa0-131">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e6fa0-131">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="e6fa0-132">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="e6fa0-132">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

