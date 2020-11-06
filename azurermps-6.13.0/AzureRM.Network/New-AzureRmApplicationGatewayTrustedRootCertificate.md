---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewaytrustedrootcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayTrustedRootCertificate.md
ms.openlocfilehash: 5f71f9a28eb1daae1bee070907675c87002241f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594875"
---
# <span data-ttu-id="858db-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="858db-101">New-AzureRmApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="858db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858db-102">SYNOPSIS</span></span>
<span data-ttu-id="858db-103">Uygulama ağ geçidi için güvenilen kök sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="858db-103">Creates a Trusted Root Certificate for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="858db-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="858db-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayTrustedRootCertificate -Name <String> -CertificateFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="858db-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="858db-105">DESCRIPTION</span></span>
<span data-ttu-id="858db-106">**New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet 'ı bir Azure Application Gateway Için güvenilen kök sertifikası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="858db-106">The **New-AzureRmApplicationGatewayTrustedRootCertificate** cmdlet creates a Trusted Root Certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="858db-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="858db-107">EXAMPLES</span></span>

### <span data-ttu-id="858db-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="858db-108">Example 1</span></span>
```powershell
PS C:\> $certFilePath = ".\rootCA.cer"
PS C:\> $trc = New-AzureRmApplicationGatewayTrustedRootCertificate -Name "trc1" --CertificateFile $certFilePath
```

<span data-ttu-id="858db-109">Bu komut, "TRC1" listesi adlı bir güvenilen kök sertifika oluşturur ve sonucu $trc adlı değişkende depolar.</span><span class="sxs-lookup"><span data-stu-id="858db-109">This command creates a Trusted Root Certificate named List "trc1" and stores the result in the variable named $trc.</span></span>

## <span data-ttu-id="858db-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="858db-110">PARAMETERS</span></span>

### <span data-ttu-id="858db-111">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="858db-111">-CertificateFile</span></span>
<span data-ttu-id="858db-112">Sertifika CER dosyasının yolu</span><span class="sxs-lookup"><span data-stu-id="858db-112">Path of certificate CER file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858db-113">-DefaultProfile</span></span>
<span data-ttu-id="858db-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="858db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="858db-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="858db-115">-Name</span></span>
<span data-ttu-id="858db-116">TrustedRoot sertifikasının adı</span><span class="sxs-lookup"><span data-stu-id="858db-116">The name of the TrustedRoot certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858db-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="858db-117">-Confirm</span></span>
<span data-ttu-id="858db-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="858db-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858db-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="858db-119">-WhatIf</span></span>
<span data-ttu-id="858db-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="858db-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="858db-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="858db-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="858db-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858db-122">CommonParameters</span></span>
<span data-ttu-id="858db-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="858db-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858db-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="858db-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858db-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="858db-125">INPUTS</span></span>

### <span data-ttu-id="858db-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="858db-126">None</span></span>

## <span data-ttu-id="858db-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="858db-127">OUTPUTS</span></span>

### <span data-ttu-id="858db-128">Microsoft. Azure. Commands. Network. modeller. PSApplicationGatewayTrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="858db-128">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate</span></span>

## <span data-ttu-id="858db-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="858db-129">NOTES</span></span>

## <span data-ttu-id="858db-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="858db-130">RELATED LINKS</span></span>
