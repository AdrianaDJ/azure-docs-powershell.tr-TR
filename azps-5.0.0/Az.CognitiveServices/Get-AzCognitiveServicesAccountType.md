---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccounttype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountType.md
ms.openlocfilehash: a99ca4bb636ba1767fc5f50611d3c5a9eb991312
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94322250"
---
# <span data-ttu-id="2a47b-101">Get-AzCognitiveServicesAccountType</span><span class="sxs-lookup"><span data-stu-id="2a47b-101">Get-AzCognitiveServicesAccountType</span></span>

## <span data-ttu-id="2a47b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a47b-102">SYNOPSIS</span></span>
<span data-ttu-id="2a47b-103">Kullanılabilir öğrenme hizmeti hesap türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2a47b-103">Gets the available Cognitive Services Account Types.</span></span>

## <span data-ttu-id="2a47b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2a47b-104">SYNTAX</span></span>

### <span data-ttu-id="2a47b-105">GetAccountTypes (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2a47b-105">GetAccountTypes (Default)</span></span>
```
Get-AzCognitiveServicesAccountType [-Location <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a47b-106">GetAccountTypeWithName</span><span class="sxs-lookup"><span data-stu-id="2a47b-106">GetAccountTypeWithName</span></span>
```
Get-AzCognitiveServicesAccountType -TypeName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a47b-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2a47b-107">DESCRIPTION</span></span>
<span data-ttu-id="2a47b-108">**Get-Azöğretici Iveservicesaccounttype** cmdlet 'i, bu aboneliğin altındaki kullanılabilir öğretici hizmet hesap türlerini alır.</span><span class="sxs-lookup"><span data-stu-id="2a47b-108">The **Get-AzCognitiveServicesAccountType** cmdlet gets the available Cognitive Services Account Types under this subscription.</span></span>

## <span data-ttu-id="2a47b-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2a47b-109">EXAMPLES</span></span>

### <span data-ttu-id="2a47b-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="2a47b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType
```

<span data-ttu-id="2a47b-111">Kullanılabilir türlerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="2a47b-111">Get the list of available Types.</span></span>

### <span data-ttu-id="2a47b-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="2a47b-112">Example 2</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -Location westus
```

<span data-ttu-id="2a47b-113">Westus 'de kullanılabilir türlerin listesini alın.</span><span class="sxs-lookup"><span data-stu-id="2a47b-113">Get the list of available Types in westus.</span></span>

### <span data-ttu-id="2a47b-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="2a47b-114">Example 3</span></span>
```powershell
PS C:\> Get-AzCognitiveServicesAccountType -TypeName Face

Face
```

<span data-ttu-id="2a47b-115">`Face`Geçerli bir tür adı olup olmadığını denetleyin, ad geçerli bir adise döndürülür.</span><span class="sxs-lookup"><span data-stu-id="2a47b-115">Check if `Face` is a valid Type name, the name will be returned if it is a valid name.</span></span>

## <span data-ttu-id="2a47b-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2a47b-116">PARAMETERS</span></span>

### <span data-ttu-id="2a47b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a47b-117">-DefaultProfile</span></span>
<span data-ttu-id="2a47b-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2a47b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a47b-119">-Konum</span><span class="sxs-lookup"><span data-stu-id="2a47b-119">-Location</span></span>
<span data-ttu-id="2a47b-120">Öğretici hizmetler hesap konumu.</span><span class="sxs-lookup"><span data-stu-id="2a47b-120">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="2a47b-121">-TypeName</span><span class="sxs-lookup"><span data-stu-id="2a47b-121">-TypeName</span></span>
<span data-ttu-id="2a47b-122">Öğretici hizmetler hesap türü adı.</span><span class="sxs-lookup"><span data-stu-id="2a47b-122">Cognitive Services Account Type Name.</span></span>

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

### <span data-ttu-id="2a47b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a47b-123">CommonParameters</span></span>
<span data-ttu-id="2a47b-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2a47b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a47b-125">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2a47b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a47b-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2a47b-126">INPUTS</span></span>

### <span data-ttu-id="2a47b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2a47b-127">System.String</span></span>

## <span data-ttu-id="2a47b-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2a47b-128">OUTPUTS</span></span>

### <span data-ttu-id="2a47b-129">System. String []</span><span class="sxs-lookup"><span data-stu-id="2a47b-129">System.String[]</span></span>

### <span data-ttu-id="2a47b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2a47b-130">System.String</span></span>

## <span data-ttu-id="2a47b-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2a47b-131">NOTES</span></span>

## <span data-ttu-id="2a47b-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2a47b-132">RELATED LINKS</span></span>
