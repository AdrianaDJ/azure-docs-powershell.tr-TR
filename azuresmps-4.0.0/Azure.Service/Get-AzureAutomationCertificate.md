---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: FED10AA9-DD3A-4034-B78E-F9E55290B353
online version: ''
schema: 2.0.0
ms.openlocfilehash: 272969751988d3747788c2a214e8eb7ed509f232
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105663"
---
# <span data-ttu-id="f0686-101">Get-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0686-101">Get-AzureAutomationCertificate</span></span>

## <span data-ttu-id="f0686-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0686-102">SYNOPSIS</span></span>

<span data-ttu-id="f0686-103">Bir Azure Otomasyonu sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="f0686-103">Gets an Azure Automation certificate.</span></span>

## <span data-ttu-id="f0686-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f0686-104">SYNTAX</span></span>

### <span data-ttu-id="f0686-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f0686-105">ByAll (Default)</span></span>
```
Get-AzureAutomationCertificate -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f0686-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="f0686-106">ByCertificateName</span></span>
```
Get-AzureAutomationCertificate -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0686-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f0686-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="f0686-108">**Get-AzureAutomationCertificate** cmdlet 'i bir veya daha fazla Microsoft Azure Automation sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="f0686-108">The **Get-AzureAutomationCertificate** cmdlet gets one or more Microsoft Azure Automation certificates.</span></span>
<span data-ttu-id="f0686-109">Varsayılan olarak, tüm sertifikalar verilir.</span><span class="sxs-lookup"><span data-stu-id="f0686-109">By default, all certificates are returned.</span></span>
<span data-ttu-id="f0686-110">Belirli bir sertifikayı almak için adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="f0686-110">To get a specific certificate, specify its name.</span></span>

## <span data-ttu-id="f0686-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f0686-111">EXAMPLES</span></span>

### <span data-ttu-id="f0686-112">Örnek 1: tüm sertifikaları al</span><span class="sxs-lookup"><span data-stu-id="f0686-112">Example 1: Get all certificates</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17"
```

<span data-ttu-id="f0686-113">Bu komut, Contoso17 adlı Azure Otomasyonu hesabındaki tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="f0686-113">This command gets all certificates in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="f0686-114">Örnek 2: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="f0686-114">Example 2: Get a certificate</span></span>
```
PS C:\> Get-AzureAutomationCertificate -AutomationAccountName "Contoso17" -Name "MyUserCertificate"
```

<span data-ttu-id="f0686-115">Bu komut MyUserCertificate adlı sertifikayı alır.</span><span class="sxs-lookup"><span data-stu-id="f0686-115">This command gets the certificate named MyUserCertificate.</span></span>

## <span data-ttu-id="f0686-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f0686-116">PARAMETERS</span></span>

### <span data-ttu-id="f0686-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f0686-117">-AutomationAccountName</span></span>
<span data-ttu-id="f0686-118">Sertifikayla birlikte Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0686-118">Specifies the name of the automation account with the certificate.</span></span>

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

### <span data-ttu-id="f0686-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="f0686-119">-Name</span></span>
<span data-ttu-id="f0686-120">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0686-120">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0686-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="f0686-121">-Profile</span></span>
<span data-ttu-id="f0686-122">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f0686-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f0686-123">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="f0686-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f0686-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0686-124">CommonParameters</span></span>
<span data-ttu-id="f0686-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f0686-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0686-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0686-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0686-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f0686-127">INPUTS</span></span>

## <span data-ttu-id="f0686-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f0686-128">OUTPUTS</span></span>

### <span data-ttu-id="f0686-129">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="f0686-129">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="f0686-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f0686-130">NOTES</span></span>

## <span data-ttu-id="f0686-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f0686-131">RELATED LINKS</span></span>

[<span data-ttu-id="f0686-132">Yeni-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0686-132">New-AzureAutomationCertificate</span></span>](./New-AzureAutomationCertificate.md)

[<span data-ttu-id="f0686-133">Remove-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0686-133">Remove-AzureAutomationCertificate</span></span>](./Remove-AzureAutomationCertificate.md)

[<span data-ttu-id="f0686-134">Set-AzureAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="f0686-134">Set-AzureAutomationCertificate</span></span>](./Set-AzureAutomationCertificate.md)


