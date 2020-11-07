---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 956569d407918d0891af6aa1d6f8f09eb61b9a98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764277"
---
# <span data-ttu-id="3ed65-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3ed65-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="3ed65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ed65-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed65-103">Otomasyon sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="3ed65-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ed65-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3ed65-104">SYNTAX</span></span>

### <span data-ttu-id="3ed65-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3ed65-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3ed65-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="3ed65-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3ed65-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="3ed65-107">DESCRIPTION</span></span>
<span data-ttu-id="3ed65-108">**Get-AzureRmAutomationCertificate** cmdlet 'i, bir veya daha fazla Azure Automation sertifikasını alır.</span><span class="sxs-lookup"><span data-stu-id="3ed65-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="3ed65-109">Varsayılan olarak, bu cmdlet tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="3ed65-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="3ed65-110">Belirli bir sertifikanın alınacağı sertifikanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="3ed65-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="3ed65-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3ed65-111">EXAMPLES</span></span>

### <span data-ttu-id="3ed65-112">Örnek 1: tüm sertifikaları al</span><span class="sxs-lookup"><span data-stu-id="3ed65-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="3ed65-113">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm sertifikaların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ed65-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="3ed65-114">Örnek 2: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="3ed65-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="3ed65-115">Bu komut, ContosoCertificate adlı sertifikanın meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="3ed65-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="3ed65-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3ed65-116">PARAMETERS</span></span>

### <span data-ttu-id="3ed65-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3ed65-117">-AutomationAccountName</span></span>
<span data-ttu-id="3ed65-118">Bu cmdlet 'in sertifika aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ed65-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="3ed65-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="3ed65-119">-Name</span></span>
<span data-ttu-id="3ed65-120">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ed65-120">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="3ed65-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ed65-121">-ResourceGroupName</span></span>
<span data-ttu-id="3ed65-122">Bu cmdlet 'in Otomasyon sertifikası aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="3ed65-122">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="3ed65-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed65-123">-DefaultProfile</span></span>
<span data-ttu-id="3ed65-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3ed65-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ed65-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed65-125">CommonParameters</span></span>
<span data-ttu-id="3ed65-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3ed65-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed65-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ed65-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed65-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3ed65-128">INPUTS</span></span>

## <span data-ttu-id="3ed65-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3ed65-129">OUTPUTS</span></span>

### <span data-ttu-id="3ed65-130">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="3ed65-130">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="3ed65-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3ed65-131">NOTES</span></span>

## <span data-ttu-id="3ed65-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3ed65-132">RELATED LINKS</span></span>

[<span data-ttu-id="3ed65-133">Yeni-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3ed65-133">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3ed65-134">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3ed65-134">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="3ed65-135">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="3ed65-135">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


