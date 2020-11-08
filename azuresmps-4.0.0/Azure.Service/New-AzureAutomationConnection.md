---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: B7E71C5C-6329-475B-993C-A839FFEF8F98
online version: ''
schema: 2.0.0
ms.openlocfilehash: cef5d19cdb954e98fe0e97cc0042bfaf91505c0c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106220"
---
# <span data-ttu-id="9454e-101">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9454e-101">New-AzureAutomationConnection</span></span>

## <span data-ttu-id="9454e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9454e-102">SYNOPSIS</span></span>

<span data-ttu-id="9454e-103">Otomasyon 'da bir bağlantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9454e-103">Creates a connection in Automation.</span></span>

## <span data-ttu-id="9454e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9454e-104">SYNTAX</span></span>

```
New-AzureAutomationConnection -Name <String> -ConnectionTypeName <String> -ConnectionFieldValues <IDictionary>
 [-Description <String>] -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9454e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9454e-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="9454e-106">**New-AzureAutomationConnection** cmdlet 'ı Microsoft Azure Otomasyonu 'nda bir bağlantı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9454e-106">The **New-AzureAutomationConnection** cmdlet creates a connection in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="9454e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9454e-107">EXAMPLES</span></span>

## <span data-ttu-id="9454e-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9454e-108">PARAMETERS</span></span>

### <span data-ttu-id="9454e-109">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9454e-109">-AutomationAccountName</span></span>
<span data-ttu-id="9454e-110">Bağlantının saklanacağı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9454e-110">Specifies the name of the Automation account the connection will be stored in.</span></span>

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

### <span data-ttu-id="9454e-111">-ConnectionFieldValues</span><span class="sxs-lookup"><span data-stu-id="9454e-111">-ConnectionFieldValues</span></span>
<span data-ttu-id="9454e-112">Anahtar/değer çiftlerini içeren karma tabloyu belirtir.</span><span class="sxs-lookup"><span data-stu-id="9454e-112">Specifies a hash table that contains key/value pairs.</span></span>
<span data-ttu-id="9454e-113">Anahtarlar belirtilen bağlantı türündeki bağlantı alanlarını temsil eder.</span><span class="sxs-lookup"><span data-stu-id="9454e-113">The keys represent the connection fields on the specified connection type.</span></span>
<span data-ttu-id="9454e-114">Değerler, bağlantı örneği için her bağlantı alanı için depolanacak belirli değerleri temsil eder.</span><span class="sxs-lookup"><span data-stu-id="9454e-114">The values represent the specific values to store for each connection field for the connection instance.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9454e-115">-ConnectionTypeName</span><span class="sxs-lookup"><span data-stu-id="9454e-115">-ConnectionTypeName</span></span>
<span data-ttu-id="9454e-116">Bağlantı türünün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9454e-116">Specifies the name of the connection type.</span></span>

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

### <span data-ttu-id="9454e-117">-Açıklama</span><span class="sxs-lookup"><span data-stu-id="9454e-117">-Description</span></span>
<span data-ttu-id="9454e-118">Kimlik bilgisinin açıklamasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9454e-118">Specifies a description for the credential.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9454e-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9454e-119">-Name</span></span>
<span data-ttu-id="9454e-120">Bağlantı için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="9454e-120">Specifies a name for the connection.</span></span>

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

### <span data-ttu-id="9454e-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="9454e-121">-Profile</span></span>
<span data-ttu-id="9454e-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="9454e-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9454e-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="9454e-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9454e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9454e-124">CommonParameters</span></span>
<span data-ttu-id="9454e-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9454e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9454e-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9454e-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9454e-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9454e-127">INPUTS</span></span>

## <span data-ttu-id="9454e-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9454e-128">OUTPUTS</span></span>

### <span data-ttu-id="9454e-129">Microsoft. Azure. Commands. Automation. model. Connection</span><span class="sxs-lookup"><span data-stu-id="9454e-129">Microsoft.Azure.Commands.Automation.Model.Connection</span></span>

## <span data-ttu-id="9454e-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9454e-130">NOTES</span></span>

## <span data-ttu-id="9454e-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9454e-131">RELATED LINKS</span></span>

[<span data-ttu-id="9454e-132">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9454e-132">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="9454e-133">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="9454e-133">Remove-AzureAutomationConnection</span></span>](./Remove-AzureAutomationConnection.md)

[<span data-ttu-id="9454e-134">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="9454e-134">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


