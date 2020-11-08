---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: BCF8DAB4-3E14-463B-A18F-E91C740B0D3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 08dd82489bf02efa167386300b9b1d565e1a63de
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106493"
---
# <span data-ttu-id="5cb30-101">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5cb30-101">Remove-AzureAutomationCertificate</span></span>

## <span data-ttu-id="5cb30-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cb30-102">SYNOPSIS</span></span>

<span data-ttu-id="5cb30-103">Otomasyon sertifikasını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cb30-103">Removes an Automation certificate.</span></span>

## <span data-ttu-id="5cb30-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5cb30-104">SYNTAX</span></span>

```
Remove-AzureAutomationCertificate -Name <String> [-Force] -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5cb30-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5cb30-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="5cb30-106">**Remove-AzureAutomationAccount** cmdlet 'ı, Microsoft Azure Otomasyonu 'ndan sertifika kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cb30-106">The **Remove-AzureAutomationAccount** cmdlet removes a certificate from Microsoft Azure Automation.</span></span>

## <span data-ttu-id="5cb30-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5cb30-107">EXAMPLES</span></span>

### <span data-ttu-id="5cb30-108">Örnek 1: sertifikayı kaldırma</span><span class="sxs-lookup"><span data-stu-id="5cb30-108">Example 1: Remove a certificate</span></span>
```
PS C:\> Remove-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "Cert01"
```

<span data-ttu-id="5cb30-109">Bu komut, Contoso17 adındaki Otomasyon hesabındaki Cert01 adındaki sertifikayı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5cb30-109">This command removes a certificate named Cert01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5cb30-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5cb30-110">PARAMETERS</span></span>

### <span data-ttu-id="5cb30-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5cb30-111">-AutomationAccountName</span></span>
<span data-ttu-id="5cb30-112">Sertifikayla birlikte Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb30-112">Specifies the name of the Automation account with the certificate.</span></span>

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

### <span data-ttu-id="5cb30-113">-Force</span><span class="sxs-lookup"><span data-stu-id="5cb30-113">-Force</span></span>
<span data-ttu-id="5cb30-114">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="5cb30-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5cb30-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="5cb30-115">-Name</span></span>
<span data-ttu-id="5cb30-116">Sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb30-116">Specifies the name of the certificate.</span></span>

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

### <span data-ttu-id="5cb30-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="5cb30-117">-Profile</span></span>
<span data-ttu-id="5cb30-118">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5cb30-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5cb30-119">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5cb30-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5cb30-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cb30-120">CommonParameters</span></span>
<span data-ttu-id="5cb30-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5cb30-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cb30-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cb30-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cb30-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5cb30-123">INPUTS</span></span>

## <span data-ttu-id="5cb30-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5cb30-124">OUTPUTS</span></span>

## <span data-ttu-id="5cb30-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5cb30-125">NOTES</span></span>

## <span data-ttu-id="5cb30-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5cb30-126">RELATED LINKS</span></span>

[<span data-ttu-id="5cb30-127">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5cb30-127">Get-AzureAutomationCertificate</span></span>](./Get-AzureAutomationCertificate.md)

[<span data-ttu-id="5cb30-128">Yeni-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5cb30-128">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="5cb30-129">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="5cb30-129">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


