---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cognitiveservices/get-azurermcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountType.md
ms.openlocfilehash: 05a4af3e92febcf30d44de9b114972a7c1f61d5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592786"
---
# <span data-ttu-id="c0d56-101">Get-AzureRmCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="c0d56-101">Get-AzureRmCognitiveServicesAccountType</span></span>

## <span data-ttu-id="c0d56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0d56-102">SYNOPSIS</span></span>
<span data-ttu-id="c0d56-103">Kullanılabilir öğrenme hizmeti hesap türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c0d56-103">Gets the available Cognitive Services Account Types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0d56-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c0d56-104">SYNTAX</span></span>

### <span data-ttu-id="c0d56-105">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="c0d56-105">GetAccountTypeWithName</span></span>
```
Get-AzureRmCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0d56-106">GetAccountTypes</span><span class="sxs-lookup"><span data-stu-id="c0d56-106">GetAccountTypes</span></span>
```
Get-AzureRmCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c0d56-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c0d56-107">DESCRIPTION</span></span>
<span data-ttu-id="c0d56-108">**Get-Azurermöğretici Iveservicesaccounttype** cmdlet 'i, bu aboneliğin altındaki kullanılabilir öğretici hizmet hesap türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="c0d56-108">The **Get-AzureRmCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="c0d56-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c0d56-109">EXAMPLES</span></span>

### <span data-ttu-id="c0d56-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c0d56-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType
```

<span data-ttu-id="c0d56-111">Kullanılabilir türlerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="c0d56-111">Get the list of available Types.</span></span>

### <span data-ttu-id="c0d56-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c0d56-112">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="c0d56-113">Westus 'de kullanılabilir türlerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="c0d56-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="c0d56-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c0d56-114">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="c0d56-115">`Face`Geçerli bir tür adı olup olmadığını denetleyin, ad geçerli bir adise döndürülür.</span><span class="sxs-lookup"><span data-stu-id="c0d56-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="c0d56-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c0d56-116">PARAMETERS</span></span>

### <span data-ttu-id="c0d56-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0d56-117">-DefaultProfile</span></span>
<span data-ttu-id="c0d56-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c0d56-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0d56-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="c0d56-119">-Location</span></span>
<span data-ttu-id="c0d56-120">Öğretici hizmetler hesap konumu.</span><span class="sxs-lookup"><span data-stu-id="c0d56-120">Cognitive Services Account Location.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypes
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d56-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="c0d56-121">-TypeName</span></span>
<span data-ttu-id="c0d56-122">Öğretici hizmetler hesap türü adı.</span><span class="sxs-lookup"><span data-stu-id="c0d56-122">Cognitive Services Account Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetAccountTypeWithName
Aliases: CognitiveServicesAccountTypeName, AccountTypeName, KindName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0d56-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0d56-123">CommonParameters</span></span>
<span data-ttu-id="c0d56-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c0d56-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0d56-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0d56-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0d56-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c0d56-126">INPUTS</span></span>

### <span data-ttu-id="c0d56-127">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d56-127">System.String</span></span>

## <span data-ttu-id="c0d56-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c0d56-128">OUTPUTS</span></span>

### <span data-ttu-id="c0d56-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="c0d56-129">System.String[]</span></span>

### <span data-ttu-id="c0d56-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c0d56-130">System.String</span></span>

## <span data-ttu-id="c0d56-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c0d56-131">NOTES</span></span>

## <span data-ttu-id="c0d56-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c0d56-132">RELATED LINKS</span></span>
