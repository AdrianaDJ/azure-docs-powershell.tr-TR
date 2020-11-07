---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 06081209-BBE5-4F76-86F8-9CF6197938F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Install-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: b1d3d757d7970a21a2d81af9f1e08d0d8126df96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762690"
---
# <span data-ttu-id="736ee-101">Install-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="736ee-101">Install-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="736ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="736ee-102">SYNOPSIS</span></span>
<span data-ttu-id="736ee-103">Sunucu yönetimi ağ geçidi profilini yükler.</span><span class="sxs-lookup"><span data-stu-id="736ee-103">Installs a Server Management Gateway profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="736ee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="736ee-104">SYNTAX</span></span>

```
Install-AzureRmServerManagementGatewayProfile [[-InputFile] <FileInfo>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="736ee-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="736ee-105">DESCRIPTION</span></span>
<span data-ttu-id="736ee-106">**Install-AzureRmServerManagementGatewayProfile** cmdlet 'i, bir Azure Server yönetim ağ geçidi profilini doğru konuma yükler.</span><span class="sxs-lookup"><span data-stu-id="736ee-106">The **Install-AzureRmServerManagementGatewayProfile** cmdlet installs an Azure Server Management Gateway profile into the correct location.</span></span>
<span data-ttu-id="736ee-107">Bu cmdlet 'in yüklediği dosya profile.jsolarak adlandırılır.</span><span class="sxs-lookup"><span data-stu-id="736ee-107">The file that this cmdlet installs is named profile.json.</span></span>

## <span data-ttu-id="736ee-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="736ee-108">EXAMPLES</span></span>

## <span data-ttu-id="736ee-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="736ee-109">PARAMETERS</span></span>

### <span data-ttu-id="736ee-110">-GirdiDosyası</span><span class="sxs-lookup"><span data-stu-id="736ee-110">-InputFile</span></span>
<span data-ttu-id="736ee-111">Yüklenecek ağ geçidi profilini içeren yerel dosyanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="736ee-111">Specifies the name of the local file that contains the gateway profile to install.</span></span>

<span data-ttu-id="736ee-112">Bu cmdlet 'in yüklediği dosya, daha önce Save-AzureRmServerManagementGatewayProfile cmdlet ile kaydedilmiş olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="736ee-112">The file that this cmdlet installs should have been previously saved with the Save-AzureRmServerManagementGatewayProfile cmdlet.</span></span>

```yaml
Type: System.IO.FileInfo
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="736ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="736ee-113">-DefaultProfile</span></span>
<span data-ttu-id="736ee-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="736ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="736ee-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="736ee-115">CommonParameters</span></span>
<span data-ttu-id="736ee-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="736ee-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="736ee-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="736ee-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="736ee-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="736ee-118">INPUTS</span></span>

### <span data-ttu-id="736ee-119">Bilgis</span><span class="sxs-lookup"><span data-stu-id="736ee-119">FileInfo</span></span>
<span data-ttu-id="736ee-120">' Girditürü ' parametresi ardışık düzen için ' FileInfo ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="736ee-120">Parameter 'InputFile' accepts value of type 'FileInfo' from the pipeline</span></span>

## <span data-ttu-id="736ee-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="736ee-121">OUTPUTS</span></span>

## <span data-ttu-id="736ee-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="736ee-122">NOTES</span></span>

## <span data-ttu-id="736ee-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="736ee-123">RELATED LINKS</span></span>

[<span data-ttu-id="736ee-124">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="736ee-124">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="736ee-125">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="736ee-125">Save-AzureRmServerManagementGatewayProfile</span></span>](./Save-AzureRmServerManagementGatewayProfile.md)


