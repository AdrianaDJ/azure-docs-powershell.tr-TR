---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: 05c5e797fa5ed56d6397b3881b368038a3d03a4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761390"
---
# <span data-ttu-id="39875-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="39875-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="39875-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39875-102">SYNOPSIS</span></span>
<span data-ttu-id="39875-103">Kullanılabilir öğrenme hizmeti hesap türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="39875-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="39875-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="39875-104">SYNTAX</span></span>

### <span data-ttu-id="39875-105">GetAccountTypes (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="39875-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="39875-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="39875-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39875-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="39875-107">DESCRIPTION</span></span>
<span data-ttu-id="39875-108">**Get-Azöğretici Iveservicesaccounttype** cmdlet 'i, bu aboneliğin altındaki kullanılabilir öğretici hizmet hesap türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="39875-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="39875-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="39875-109">EXAMPLES</span></span>

### <span data-ttu-id="39875-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="39875-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="39875-111">Kullanılabilir türlerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="39875-111">Get the list of available Types.</span></span>

### <span data-ttu-id="39875-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="39875-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="39875-113">Westus 'de kullanılabilir türlerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="39875-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="39875-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="39875-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="39875-115">`Face`Geçerli bir tür adı olup olmadığını denetleyin, ad geçerli bir adise döndürülür.</span><span class="sxs-lookup"><span data-stu-id="39875-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="39875-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="39875-116">PARAMETERS</span></span>

### <span data-ttu-id="39875-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39875-117">-DefaultProfile</span></span>
<span data-ttu-id="39875-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="39875-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39875-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="39875-119">-Location</span></span>
<span data-ttu-id="39875-120">Öğretici hizmetler hesap konumu.</span><span class="sxs-lookup"><span data-stu-id="39875-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="39875-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="39875-121">-TypeName</span></span>
<span data-ttu-id="39875-122">Öğretici hizmetler hesap türü adı.</span><span class="sxs-lookup"><span data-stu-id="39875-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="39875-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39875-123">CommonParameters</span></span>
<span data-ttu-id="39875-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="39875-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39875-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39875-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39875-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="39875-126">INPUTS</span></span>

### <span data-ttu-id="39875-127">System. String</span><span class="sxs-lookup"><span data-stu-id="39875-127">System.String</span></span>

## <span data-ttu-id="39875-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="39875-128">OUTPUTS</span></span>

### <span data-ttu-id="39875-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="39875-129">System.String[]</span></span>

### <span data-ttu-id="39875-130">System. String</span><span class="sxs-lookup"><span data-stu-id="39875-130">System.String</span></span>

## <span data-ttu-id="39875-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="39875-131">NOTES</span></span>

## <span data-ttu-id="39875-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="39875-132">RELATED LINKS</span></span>
