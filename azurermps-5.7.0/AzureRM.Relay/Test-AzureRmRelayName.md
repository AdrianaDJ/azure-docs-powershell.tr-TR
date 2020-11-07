---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: adf7c4b7f8d80e16b49d9d55b742a55279232a07
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591635"
---
# <span data-ttu-id="c8ee4-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="c8ee4-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="c8ee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="c8ee4-103">Verilen ad alanı adının uygunluk durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="c8ee4-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8ee4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8ee4-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8ee4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8ee4-105">DESCRIPTION</span></span>
<span data-ttu-id="c8ee4-106">**Test-AzureRmRelayName** cmdlet 'ı ad alanı adının kullanılabilirliğini denetler</span><span class="sxs-lookup"><span data-stu-id="c8ee4-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="c8ee4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8ee4-107">EXAMPLES</span></span>

### <span data-ttu-id="c8ee4-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c8ee4-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability
```

### <span data-ttu-id="c8ee4-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c8ee4-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi
```

### <span data-ttu-id="c8ee4-110">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c8ee4-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123
```

<span data-ttu-id="c8ee4-111">Ad alanı adının uygunluk durumunu verir</span><span class="sxs-lookup"><span data-stu-id="c8ee4-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="c8ee4-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8ee4-112">PARAMETERS</span></span>

### <span data-ttu-id="c8ee4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8ee4-113">-DefaultProfile</span></span>
<span data-ttu-id="c8ee4-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c8ee4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8ee4-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c8ee4-115">-Namespace</span></span>
<span data-ttu-id="c8ee4-116">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="c8ee4-116">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="c8ee4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8ee4-117">CommonParameters</span></span>
<span data-ttu-id="c8ee4-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8ee4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8ee4-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8ee4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8ee4-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8ee4-120">INPUTS</span></span>

### <span data-ttu-id="c8ee4-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c8ee4-121">-Namespace</span></span>
 <span data-ttu-id="c8ee4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="c8ee4-122">System.String</span></span>

## <span data-ttu-id="c8ee4-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8ee4-123">OUTPUTS</span></span>

### <span data-ttu-id="c8ee4-124">[Microsoft. Azure. Commands. Relay. modeller. Checknamekullanılabilirliği Bilityresultattributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]</span><span class="sxs-lookup"><span data-stu-id="c8ee4-124">[Microsoft.Azure.Commands.Relay.Models.CheckNameAvailabilityResultAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]</span></span>

### <span data-ttu-id="c8ee4-125">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c8ee4-125">Example 1</span></span>
<span data-ttu-id="c8ee4-126">Ad kullanılabilir neden Iletisi</span><span class="sxs-lookup"><span data-stu-id="c8ee4-126">NameAvailable Reason Message</span></span>
------------- ------ -------
         True   None

### <span data-ttu-id="c8ee4-127">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="c8ee4-127">Example 2</span></span>
<span data-ttu-id="c8ee4-128">Ad kullanılabilir neden Iletisi</span><span class="sxs-lookup"><span data-stu-id="c8ee4-128">NameAvailable      Reason Message</span></span>
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.

### <span data-ttu-id="c8ee4-129">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="c8ee4-129">Example 3</span></span>
<span data-ttu-id="c8ee4-130">Ad kullanılabilir neden Iletisi</span><span class="sxs-lookup"><span data-stu-id="c8ee4-130">NameAvailable    Reason Message</span></span>
-------------    ------ -------
        False NameInUse The specified service namespace is not available.

## <span data-ttu-id="c8ee4-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8ee4-131">NOTES</span></span>

## <span data-ttu-id="c8ee4-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8ee4-132">RELATED LINKS</span></span>
