---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Test-AzureRmServiceBusName.md
ms.openlocfilehash: 892177efebb3a62e40f79b80b1ac67c488e048d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764225"
---
# <span data-ttu-id="097e9-101">Test-AzureRmServiceBusName</span><span class="sxs-lookup"><span data-stu-id="097e9-101">Test-AzureRmServiceBusName</span></span>

## <span data-ttu-id="097e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="097e9-102">SYNOPSIS</span></span>
<span data-ttu-id="097e9-103">Verilen ad alanı adının uygunluk durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="097e9-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="097e9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="097e9-104">SYNTAX</span></span>

```
Test-AzureRmServiceBusName [-Namespace] <String>
```

## <span data-ttu-id="097e9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="097e9-105">DESCRIPTION</span></span>
<span data-ttu-id="097e9-106">**Test-AzureRmServiceBusName** cmdlet 'ı ad alanı adının kullanılabilirliğini denetler</span><span class="sxs-lookup"><span data-stu-id="097e9-106">The **Test-AzureRmServiceBusName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="097e9-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="097e9-107">EXAMPLES</span></span>

### <span data-ttu-id="097e9-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="097e9-108">Example 1</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace TestingtheAvailability
```

### <span data-ttu-id="097e9-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="097e9-109">Example 2</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Testi
```

### <span data-ttu-id="097e9-110">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="097e9-110">Example 3</span></span>
```
PS C:\> Test-AzureRmServiceBusName -Namespace Test123
```

<span data-ttu-id="097e9-111">Ad alanı adının uygunluk durumunu verir</span><span class="sxs-lookup"><span data-stu-id="097e9-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="097e9-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="097e9-112">PARAMETERS</span></span>

### <span data-ttu-id="097e9-113">-Namespace</span><span class="sxs-lookup"><span data-stu-id="097e9-113">-Namespace</span></span>
<span data-ttu-id="097e9-114">ServiceBus ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="097e9-114">ServiceBus Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```
### <span data-ttu-id="097e9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="097e9-115">CommonParameters</span></span>
<span data-ttu-id="097e9-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="097e9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="097e9-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="097e9-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="097e9-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="097e9-118">INPUTS</span></span>

### <span data-ttu-id="097e9-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="097e9-119">-Namespace</span></span>
 <span data-ttu-id="097e9-120">System. String</span><span class="sxs-lookup"><span data-stu-id="097e9-120">System.String</span></span>

## <span data-ttu-id="097e9-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="097e9-121">OUTPUTS</span></span>

### <span data-ttu-id="097e9-122">[Microsoft. Azure. Commands. ServiceBus. modeller. Checknamekullanılabilirliği Bilityresultattributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.1.0.0, Culture = neutral = neutral = NULL]</span><span class="sxs-lookup"><span data-stu-id="097e9-122">[Microsoft.Azure.Commands.ServiceBus.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="097e9-123">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="097e9-123">Example 1</span></span>
<span data-ttu-id="097e9-124">Ad kullanılabilir neden Iletisi</span><span class="sxs-lookup"><span data-stu-id="097e9-124">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="097e9-125">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="097e9-125">Example 2</span></span>
<span data-ttu-id="097e9-126">Ad kullanılabilir neden Iletisi</span><span class="sxs-lookup"><span data-stu-id="097e9-126">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="097e9-127">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="097e9-127">Example 3</span></span>
<span data-ttu-id="097e9-128">Ad kullanılabilir neden Iletisi</span><span class="sxs-lookup"><span data-stu-id="097e9-128">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="097e9-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="097e9-129">NOTES</span></span>

## <span data-ttu-id="097e9-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="097e9-130">RELATED LINKS</span></span>
