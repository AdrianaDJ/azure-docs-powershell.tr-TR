---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098200"
---
# <span data-ttu-id="81757-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="81757-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="81757-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81757-102">SYNOPSIS</span></span>
<span data-ttu-id="81757-103">Otomasyon sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="81757-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="81757-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="81757-104">SYNTAX</span></span>

### <span data-ttu-id="81757-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="81757-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81757-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="81757-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81757-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="81757-107">DESCRIPTION</span></span>
<span data-ttu-id="81757-108">**Get-AzAutomationCertificate** cmdlet 'i bir veya daha fazla Azure Automation sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="81757-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="81757-109">Varsayılan olarak, bu cmdlet tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="81757-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="81757-110">Belirli bir sertifikanın alınacağı sertifikanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="81757-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="81757-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="81757-111">EXAMPLES</span></span>

### <span data-ttu-id="81757-112">Örnek 1: tüm sertifikaları al</span><span class="sxs-lookup"><span data-stu-id="81757-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="81757-113">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm sertifikaların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="81757-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="81757-114">Örnek 2: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="81757-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="81757-115">Bu komut, ContosoCertificate adlı sertifikanın meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="81757-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="81757-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="81757-116">PARAMETERS</span></span>

### <span data-ttu-id="81757-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="81757-117">-AutomationAccountName</span></span>
<span data-ttu-id="81757-118">Bu cmdlet 'in sertifika aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81757-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81757-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81757-119">-DefaultProfile</span></span>
<span data-ttu-id="81757-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="81757-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="81757-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="81757-121">-Name</span></span>
<span data-ttu-id="81757-122">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81757-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="81757-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81757-123">-ResourceGroupName</span></span>
<span data-ttu-id="81757-124">Bu cmdlet 'in Otomasyon sertifikası aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="81757-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="81757-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81757-125">CommonParameters</span></span>
<span data-ttu-id="81757-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="81757-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81757-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81757-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81757-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="81757-128">INPUTS</span></span>

### <span data-ttu-id="81757-129">System. String</span><span class="sxs-lookup"><span data-stu-id="81757-129">System.String</span></span>

## <span data-ttu-id="81757-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="81757-130">OUTPUTS</span></span>

### <span data-ttu-id="81757-131">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="81757-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="81757-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="81757-132">NOTES</span></span>

## <span data-ttu-id="81757-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="81757-133">RELATED LINKS</span></span>

[<span data-ttu-id="81757-134">Yeni-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="81757-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="81757-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="81757-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="81757-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="81757-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


