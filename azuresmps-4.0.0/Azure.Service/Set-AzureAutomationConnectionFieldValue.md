---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: F80F20B6-21CB-4A37-9CBC-277F6EE99D4B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 421e33bbc74cd70ae6959feb93a0f95f6eac1caf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106427"
---
# <span data-ttu-id="1017f-101">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="1017f-101">Set-AzureAutomationConnectionFieldValue</span></span>

## <span data-ttu-id="1017f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1017f-102">SYNOPSIS</span></span>

<span data-ttu-id="1017f-103">Bir bağlantı için alanın değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1017f-103">Modifies the value of a field for a connection.</span></span>

## <span data-ttu-id="1017f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="1017f-104">SYNTAX</span></span>

```
Set-AzureAutomationConnectionFieldValue -Name <String> -ConnectionFieldName <String> -Value <Object>
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1017f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="1017f-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1017f-106">**Set-AzureAutomationConnectionFieldValue** cmdlet 'ı, Azure Otomasyonu 'nda bir bağlantı için alan değerini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="1017f-106">The **Set-AzureAutomationConnectionFieldValue** cmdlet modifies the value for a field for a connection in Azure Automation.</span></span>

## <span data-ttu-id="1017f-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="1017f-107">EXAMPLES</span></span>

## <span data-ttu-id="1017f-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="1017f-108">PARAMETERS</span></span>

### <span data-ttu-id="1017f-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1017f-109">-AutomationAccountName</span></span>
<span data-ttu-id="1017f-110">İlgili Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="1017f-110">Specifies the name of the Automation account with the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1017f-111">-ConnectionFieldName</span><span class="sxs-lookup"><span data-stu-id="1017f-111">-ConnectionFieldName</span></span>
<span data-ttu-id="1017f-112">Alan için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="1017f-112">Specifies a name for the field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1017f-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="1017f-113">-Name</span></span>
<span data-ttu-id="1017f-114">Bağlantı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="1017f-114">Specifies a name for the connection.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1017f-115">-Profil</span><span class="sxs-lookup"><span data-stu-id="1017f-115">-Profile</span></span>
<span data-ttu-id="1017f-116">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="1017f-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1017f-117">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="1017f-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1017f-118">-Değer</span><span class="sxs-lookup"><span data-stu-id="1017f-118">-Value</span></span>
<span data-ttu-id="1017f-119">Bağlantı alanında depolanacağı değeri belirtir.</span><span class="sxs-lookup"><span data-stu-id="1017f-119">Specifies a value to store in the connection field.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1017f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1017f-120">CommonParameters</span></span>
<span data-ttu-id="1017f-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="1017f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1017f-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1017f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1017f-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="1017f-123">INPUTS</span></span>

## <span data-ttu-id="1017f-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="1017f-124">OUTPUTS</span></span>

## <span data-ttu-id="1017f-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="1017f-125">NOTES</span></span>

## <span data-ttu-id="1017f-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="1017f-126">RELATED LINKS</span></span>

[<span data-ttu-id="1017f-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1017f-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="1017f-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1017f-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="1017f-129">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="1017f-129">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)


