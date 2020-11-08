---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DDEBA3E1-B5A3-4F16-9A67-A95D15851A33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0899349c3dbfa368b3ce0dbb4d4085c3ea527c43
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106492"
---
# <span data-ttu-id="b1e70-101">Remove-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b1e70-101">Remove-AzureAutomationConnection</span></span>

## <span data-ttu-id="b1e70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1e70-102">SYNOPSIS</span></span>

<span data-ttu-id="b1e70-103">Otomasyon 'dan bir bağlantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b1e70-103">Removes a connection from Automation.</span></span>

## <span data-ttu-id="b1e70-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b1e70-104">SYNTAX</span></span>

```
Remove-AzureAutomationConnection -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b1e70-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b1e70-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="b1e70-106">**Remove-AzureAutomationConnection** cmdlet 'ı, Microsoft Azure Otomasyonu 'ndan bağlantı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b1e70-106">The **Remove-AzureAutomationConnection** cmdlet removes a connection from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="b1e70-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b1e70-107">EXAMPLES</span></span>

### <span data-ttu-id="b1e70-108">Örnek 1: bağlantı kaldırma</span><span class="sxs-lookup"><span data-stu-id="b1e70-108">Example 1: Remove a connection</span></span>
```
PS C:\> Remove-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "MyConnection"
```

<span data-ttu-id="b1e70-109">Bu komut, Contoso17 adlı Otomasyon hesabındaki MyConnection adlı sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b1e70-109">This command removes a certificate named MyConnection in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b1e70-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b1e70-110">PARAMETERS</span></span>

### <span data-ttu-id="b1e70-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b1e70-111">-AutomationAccountName</span></span>
<span data-ttu-id="b1e70-112">Kimlik bilgisiyle Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1e70-112">Specifies the name of the Automation account with the credential.</span></span>

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

### <span data-ttu-id="b1e70-113">-Force</span><span class="sxs-lookup"><span data-stu-id="b1e70-113">-Force</span></span>
<span data-ttu-id="b1e70-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="b1e70-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1e70-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="b1e70-115">-Name</span></span>
<span data-ttu-id="b1e70-116">Bağlantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1e70-116">Specifies the name of the connection.</span></span>

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

### <span data-ttu-id="b1e70-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="b1e70-117">-Profile</span></span>
<span data-ttu-id="b1e70-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b1e70-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1e70-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b1e70-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1e70-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1e70-120">CommonParameters</span></span>
<span data-ttu-id="b1e70-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b1e70-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1e70-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1e70-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1e70-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b1e70-123">INPUTS</span></span>

## <span data-ttu-id="b1e70-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b1e70-124">OUTPUTS</span></span>

## <span data-ttu-id="b1e70-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b1e70-125">NOTES</span></span>

## <span data-ttu-id="b1e70-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b1e70-126">RELATED LINKS</span></span>

[<span data-ttu-id="b1e70-127">Get-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b1e70-127">Get-AzureAutomationConnection</span></span>](./Get-AzureAutomationConnection.md)

[<span data-ttu-id="b1e70-128">New-AzureAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="b1e70-128">New-AzureAutomationConnection</span></span>](./New-AzureAutomationConnection.md)

[<span data-ttu-id="b1e70-129">Set-AzureAutomationConnectionFieldValue</span><span class="sxs-lookup"><span data-stu-id="b1e70-129">Set-AzureAutomationConnectionFieldValue</span></span>](./Set-AzureAutomationConnectionFieldValue.md)


