---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 6AC9DA05-756D-4D59-BD97-DBAAFBB3C7AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADAppCredential.md
ms.openlocfilehash: e270a59e3799302eed49a0fd60180bb8d4589d92
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594584"
---
# <span data-ttu-id="668b9-101">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="668b9-101">Get-AzureRmADAppCredential</span></span>

## <span data-ttu-id="668b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="668b9-102">SYNOPSIS</span></span>
<span data-ttu-id="668b9-103">Uygulamayla ilişkili kimlik bilgilerinin listesini alır.</span><span class="sxs-lookup"><span data-stu-id="668b9-103">Retrieves a list of credentials associated with an application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="668b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="668b9-104">SYNTAX</span></span>

### <span data-ttu-id="668b9-105">Applicationobjectivseçparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="668b9-105">ApplicationObjectIdParameterSet (Default)</span></span>
```
Get-AzureRmADAppCredential -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="668b9-106">Applicationıdparameterset</span><span class="sxs-lookup"><span data-stu-id="668b9-106">ApplicationIdParameterSet</span></span>
```
Get-AzureRmADAppCredential -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="668b9-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="668b9-107">DESCRIPTION</span></span>
<span data-ttu-id="668b9-108">Bir uygulamayla ilişkili kimlik bilgilerinin listesini almak için Get-AzureRmADAppCredential cmdlet 'i kullanılabilir.</span><span class="sxs-lookup"><span data-stu-id="668b9-108">The Get-AzureRmADAppCredential cmdlet can be used to retrieve a list of credentials associated with an application.</span></span>

<span data-ttu-id="668b9-109">Bu komut, uygulamayla ilişkili tüm kimlik bilgileri (kimlik bilgileri değerini değil) alır.</span><span class="sxs-lookup"><span data-stu-id="668b9-109">This command will retrieve all of the credential properties (but not the credential value) associated with the application.</span></span>

## <span data-ttu-id="668b9-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="668b9-110">EXAMPLES</span></span>

### <span data-ttu-id="668b9-111">--------------------------Örnek 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="668b9-111">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> Get-AzureRmADAppCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476
```

<span data-ttu-id="668b9-112">Nesne kimliği ' 1f99cf81-0146-4f4e-Val e-2007vseç0668476 ' olan uygulamayla ilişkili kimlik bilgileri listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="668b9-112">Returns a list of credentials associated with the application having object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

## <span data-ttu-id="668b9-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="668b9-113">PARAMETERS</span></span>

### <span data-ttu-id="668b9-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="668b9-114">-ApplicationId</span></span>
<span data-ttu-id="668b9-115">Kimlik bilgilerinin alınacağı uygulamanın kimliği.</span><span class="sxs-lookup"><span data-stu-id="668b9-115">The id of the application to retrieve credentials from.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="668b9-116">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="668b9-116">-ObjectId</span></span>
<span data-ttu-id="668b9-117">Kimlik bilgilerinin alınacağı uygulamanın nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="668b9-117">The object id of the application to retrieve credentials from.</span></span>

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

### <span data-ttu-id="668b9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="668b9-118">-DefaultProfile</span></span>
<span data-ttu-id="668b9-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="668b9-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="668b9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="668b9-120">CommonParameters</span></span>
<span data-ttu-id="668b9-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="668b9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="668b9-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="668b9-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="668b9-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="668b9-123">INPUTS</span></span>

## <span data-ttu-id="668b9-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="668b9-124">OUTPUTS</span></span>

### <span data-ttu-id="668b9-125">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="668b9-125">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="668b9-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="668b9-126">NOTES</span></span>

## <span data-ttu-id="668b9-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="668b9-127">RELATED LINKS</span></span>

[<span data-ttu-id="668b9-128">Yeni-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="668b9-128">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="668b9-129">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="668b9-129">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="668b9-130">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="668b9-130">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

