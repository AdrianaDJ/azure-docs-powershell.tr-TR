---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94276438"
---
# <span data-ttu-id="ed0fc-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed0fc-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="ed0fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed0fc-102">SYNOPSIS</span></span>
<span data-ttu-id="ed0fc-103">Otomasyon sertifikalarını alır.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="ed0fc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ed0fc-104">SYNTAX</span></span>

### <span data-ttu-id="ed0fc-105">Tümü (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="ed0fc-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed0fc-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="ed0fc-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed0fc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="ed0fc-107">DESCRIPTION</span></span>
<span data-ttu-id="ed0fc-108">**Get-AzAutomationCertificate** cmdlet 'i bir veya daha fazla Azure Automation sertifikası alır.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="ed0fc-109">Varsayılan olarak, bu cmdlet tüm sertifikaları alır.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="ed0fc-110">Belirli bir sertifikanın alınacağı sertifikanın adını belirtin.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="ed0fc-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ed0fc-111">EXAMPLES</span></span>

### <span data-ttu-id="ed0fc-112">Örnek 1: tüm sertifikaları al</span><span class="sxs-lookup"><span data-stu-id="ed0fc-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="ed0fc-113">Bu komut, Contoso17 adlı Otomasyon hesabındaki tüm sertifikaların meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="ed0fc-114">Örnek 2: sertifika alma</span><span class="sxs-lookup"><span data-stu-id="ed0fc-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="ed0fc-115">Bu komut, ContosoCertificate adlı sertifikanın meta verilerini alır.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="ed0fc-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ed0fc-116">PARAMETERS</span></span>

### <span data-ttu-id="ed0fc-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ed0fc-117">-AutomationAccountName</span></span>
<span data-ttu-id="ed0fc-118">Bu cmdlet 'in sertifika aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="ed0fc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed0fc-119">-DefaultProfile</span></span>
<span data-ttu-id="ed0fc-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ed0fc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed0fc-121">-Ad</span><span class="sxs-lookup"><span data-stu-id="ed0fc-121">-Name</span></span>
<span data-ttu-id="ed0fc-122">Alınacak sertifikanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="ed0fc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed0fc-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed0fc-124">Bu cmdlet 'in Otomasyon sertifikası aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="ed0fc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed0fc-125">CommonParameters</span></span>
<span data-ttu-id="ed0fc-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ed0fc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed0fc-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed0fc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed0fc-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ed0fc-128">INPUTS</span></span>

### <span data-ttu-id="ed0fc-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ed0fc-129">System.String</span></span>

## <span data-ttu-id="ed0fc-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ed0fc-130">OUTPUTS</span></span>

### <span data-ttu-id="ed0fc-131">Microsoft. Azure. Commands. Automation. model. Certificateınfo</span><span class="sxs-lookup"><span data-stu-id="ed0fc-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="ed0fc-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ed0fc-132">NOTES</span></span>

## <span data-ttu-id="ed0fc-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ed0fc-133">RELATED LINKS</span></span>

[<span data-ttu-id="ed0fc-134">Yeni-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed0fc-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="ed0fc-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed0fc-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="ed0fc-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="ed0fc-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


