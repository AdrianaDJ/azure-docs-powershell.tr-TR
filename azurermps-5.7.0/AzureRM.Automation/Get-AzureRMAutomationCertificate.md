---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 012eb357b6d64964c2564dca51ac0b77a5f96880
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587717"
---
# <span data-ttu-id="38b3e-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="38b3e-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="38b3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38b3e-102">SYNOPSIS</span></span>
<span data-ttu-id="38b3e-103">Otomasyon sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="38b3e-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38b3e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="38b3e-104">SYNTAX</span></span>

### <span data-ttu-id="38b3e-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="38b3e-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38b3e-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="38b3e-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38b3e-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="38b3e-107">DESCRIPTION</span></span>
<span data-ttu-id="38b3e-108">**Get-AzureRmAutomationCertificate** cmdlet 'i, bir veya daha fazla Azure Automation sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="38b3e-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="38b3e-109">Varsayılan olarak, bu cmdlet tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="38b3e-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="38b3e-110">Belirli bir sertifikanın alınacağı sertifikanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="38b3e-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="38b3e-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="38b3e-111">EXAMPLES</span></span>

### <span data-ttu-id="38b3e-112">Örnek 1: tüm sertifikaları al</span><span class="sxs-lookup"><span data-stu-id="38b3e-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="38b3e-113">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm sertifikaların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="38b3e-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="38b3e-114">Örnek 2: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="38b3e-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="38b3e-115">Bu komut, ContosoCertificate adlı sertifikanın meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="38b3e-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="38b3e-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="38b3e-116">PARAMETERS</span></span>

### <span data-ttu-id="38b3e-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38b3e-117">-AutomationAccountName</span></span>
<span data-ttu-id="38b3e-118">Bu cmdlet 'in sertifika aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b3e-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b3e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38b3e-119">-DefaultProfile</span></span>
<span data-ttu-id="38b3e-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="38b3e-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38b3e-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="38b3e-121">-Name</span></span>
<span data-ttu-id="38b3e-122">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b3e-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38b3e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38b3e-123">-ResourceGroupName</span></span>
<span data-ttu-id="38b3e-124">Bu cmdlet 'in Otomasyon sertifikası aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="38b3e-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="38b3e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38b3e-125">CommonParameters</span></span>
<span data-ttu-id="38b3e-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="38b3e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38b3e-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38b3e-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38b3e-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="38b3e-128">INPUTS</span></span>

### <span data-ttu-id="38b3e-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="38b3e-129">None</span></span>
<span data-ttu-id="38b3e-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="38b3e-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38b3e-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="38b3e-131">OUTPUTS</span></span>

### <span data-ttu-id="38b3e-132">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="38b3e-132">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="38b3e-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="38b3e-133">NOTES</span></span>

## <span data-ttu-id="38b3e-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="38b3e-134">RELATED LINKS</span></span>

[<span data-ttu-id="38b3e-135">Yeni-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="38b3e-135">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="38b3e-136">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="38b3e-136">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="38b3e-137">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="38b3e-137">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


