---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/test-azurermrelayname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Test-AzureRmRelayName.md
ms.openlocfilehash: 396243e366f6a21e2ac94d105473b348c6a8198d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592742"
---
# <span data-ttu-id="7ae50-101">Test-AzureRmRelayName</span><span class="sxs-lookup"><span data-stu-id="7ae50-101">Test-AzureRmRelayName</span></span>

## <span data-ttu-id="7ae50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ae50-102">SYNOPSIS</span></span>
<span data-ttu-id="7ae50-103">Verilen ad alanı adının uygunluk durumunu denetler</span><span class="sxs-lookup"><span data-stu-id="7ae50-103">Checks the Availability of the given NameSpace Name</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ae50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7ae50-104">SYNTAX</span></span>

```
Test-AzureRmRelayName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ae50-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7ae50-105">DESCRIPTION</span></span>
<span data-ttu-id="7ae50-106">**Test-AzureRmRelayName** cmdlet 'ı ad alanı adının kullanılabilirliğini denetler</span><span class="sxs-lookup"><span data-stu-id="7ae50-106">The **Test-AzureRmRelayName** Cmdlet Check Availability of the NameSpace Name</span></span>

## <span data-ttu-id="7ae50-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7ae50-107">EXAMPLES</span></span>

### <span data-ttu-id="7ae50-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7ae50-108">Example 1</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace TestingtheAvailability

NameAvailable Reason Message
------------- ------ -------
         True   None
```

### <span data-ttu-id="7ae50-109">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="7ae50-109">Example 2</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Testi

NameAvailable      Reason Message
-------------      ------ -------
        False InvalidName The specified service namespace is invalid.
```

### <span data-ttu-id="7ae50-110">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="7ae50-110">Example 3</span></span>
```
PS C:\> Test-AzureRmRelayName -Namespace Test123

NameAvailable    Reason Message
-------------    ------ -------
        False NameInUse The specified service namespace is not available.
```

<span data-ttu-id="7ae50-111">Ad alanı adının uygunluk durumunu verir</span><span class="sxs-lookup"><span data-stu-id="7ae50-111">Returns the status on availability of the namespace name</span></span>

## <span data-ttu-id="7ae50-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7ae50-112">PARAMETERS</span></span>

### <span data-ttu-id="7ae50-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ae50-113">-DefaultProfile</span></span>
<span data-ttu-id="7ae50-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7ae50-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ae50-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7ae50-115">-Namespace</span></span>
<span data-ttu-id="7ae50-116">Geçiş ad alanı adı.</span><span class="sxs-lookup"><span data-stu-id="7ae50-116">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ae50-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ae50-117">CommonParameters</span></span>
<span data-ttu-id="7ae50-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7ae50-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7ae50-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ae50-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ae50-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7ae50-120">INPUTS</span></span>

### <span data-ttu-id="7ae50-121">System. String</span><span class="sxs-lookup"><span data-stu-id="7ae50-121">System.String</span></span>


## <span data-ttu-id="7ae50-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7ae50-122">OUTPUTS</span></span>

### <span data-ttu-id="7ae50-123">Microsoft. Azure. Commands. Relay. model. Pschecknamekullanılabilirliği Bilityresultattributes</span><span class="sxs-lookup"><span data-stu-id="7ae50-123">Microsoft.Azure.Commands.Relay.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="7ae50-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7ae50-124">NOTES</span></span>

## <span data-ttu-id="7ae50-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7ae50-125">RELATED LINKS</span></span>
