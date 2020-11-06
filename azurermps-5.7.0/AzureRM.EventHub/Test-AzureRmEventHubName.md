---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/test-azurermeventhubname
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Test-AzureRmEventHubName.md
ms.openlocfilehash: e1b6de255896adbf8fd47eb57973b5c5df0d79a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589787"
---
# <span data-ttu-id="d57b5-101">Test-AzureRmEventHubName</span><span class="sxs-lookup"><span data-stu-id="d57b5-101">Test-AzureRmEventHubName</span></span>

## <span data-ttu-id="d57b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d57b5-102">SYNOPSIS</span></span>
<span data-ttu-id="d57b5-103">Verilen ad alanı adının veya diğer adın uygunluk durumunu denetler (DR yapılandırma adı)</span><span class="sxs-lookup"><span data-stu-id="d57b5-103">Checks the Availability of the given NameSpace Name or Alias (DR Configuration Name)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d57b5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d57b5-104">SYNTAX</span></span>

### <span data-ttu-id="d57b5-105">Namespacechecknamekullanılabilirliği Bilityset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d57b5-105">NamespaceCheckNameAvailabilitySet (Default)</span></span>
```
Test-AzureRmEventHubName [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d57b5-106">Diğerad</span><span class="sxs-lookup"><span data-stu-id="d57b5-106">AliasCheckNameAvailabilitySet</span></span>
```
Test-AzureRmEventHubName [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d57b5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="d57b5-107">DESCRIPTION</span></span>
<span data-ttu-id="d57b5-108">**Test-AzureRmEventhubName** cmdlet 'i</span><span class="sxs-lookup"><span data-stu-id="d57b5-108">The **Test-AzureRmEventhubName** Cmdlet Check Availability of the NameSpace Name or Alias (DR Configuration Name)</span></span>

## <span data-ttu-id="d57b5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d57b5-109">EXAMPLES</span></span>

### <span data-ttu-id="d57b5-110">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d57b5-110">Example 1</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="d57b5-111">' MyNameSapceName ' ad alanı adının kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="d57b5-111">Returns the status on availability of the namespace name 'MyNameSapceName' as True</span></span>

### <span data-ttu-id="d57b5-112">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d57b5-112">Example 2</span></span>
```
PS C:\> Test-AzureRmEventhubName -Namespace MyNameSapceName
```

<span data-ttu-id="d57b5-113">' MyNameSapceName ' ad alanı adının kullanılabilirliği nedeniyle durumu yanlış olarak verir</span><span class="sxs-lookup"><span data-stu-id="d57b5-113">Returns the status on availability of the namespace name 'MyNameSapceName' as False with Reason</span></span>

### <span data-ttu-id="d57b5-114">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="d57b5-114">Example 3</span></span>
```
PS C:\> Test-AzureRmEventhubName -ResourceGroupName MyResourceGroup -Namespace Test123 -AliasName myAliasName
```

<span data-ttu-id="d57b5-115">' MyNameSapceName ' ad alanı altındaki ' myAliasName ' diğer ad adının kullanılabilirliği</span><span class="sxs-lookup"><span data-stu-id="d57b5-115">Returns the status on availability of the alias name 'myAliasName' under namespace 'MyNameSapceName' as True</span></span>

## <span data-ttu-id="d57b5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d57b5-116">PARAMETERS</span></span>

### <span data-ttu-id="d57b5-117">-Diğerad</span><span class="sxs-lookup"><span data-stu-id="d57b5-117">-AliasName</span></span>
<span data-ttu-id="d57b5-118">DR yapılandırma adı-diğer ad</span><span class="sxs-lookup"><span data-stu-id="d57b5-118">DR Configuration Name - Alias Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d57b5-119">-DefaultProfile</span></span>
<span data-ttu-id="d57b5-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d57b5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d57b5-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d57b5-121">-Namespace</span></span>
<span data-ttu-id="d57b5-122">Eventhub ad alanı adı</span><span class="sxs-lookup"><span data-stu-id="d57b5-122">Eventhub Namespace Name</span></span>

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

### <span data-ttu-id="d57b5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d57b5-123">-ResourceGroupName</span></span>
<span data-ttu-id="d57b5-124">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="d57b5-124">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: AliasCheckNameAvailabilitySet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d57b5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d57b5-125">CommonParameters</span></span>
<span data-ttu-id="d57b5-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d57b5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d57b5-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d57b5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d57b5-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d57b5-128">INPUTS</span></span>

### <span data-ttu-id="d57b5-129">System. String</span><span class="sxs-lookup"><span data-stu-id="d57b5-129">System.String</span></span>


## <span data-ttu-id="d57b5-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d57b5-130">OUTPUTS</span></span>

### <span data-ttu-id="d57b5-131">Microsoft. Azure. Commands. EventHub. model. Pschecknamekullanılabilirliği Bilityresultattributes</span><span class="sxs-lookup"><span data-stu-id="d57b5-131">Microsoft.Azure.Commands.EventHub.Models.PSCheckNameAvailabilityResultAttributes</span></span>


## <span data-ttu-id="d57b5-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d57b5-132">NOTES</span></span>

## <span data-ttu-id="d57b5-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d57b5-133">RELATED LINKS</span></span>
