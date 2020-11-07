---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/new-azurermservermanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: f73d53fc3031fc72be950547e5b9c2b93a9a0079
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762358"
---
# <span data-ttu-id="dade8-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="dade8-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="dade8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dade8-102">SYNOPSIS</span></span>
<span data-ttu-id="dade8-103">Sunucu yönetimi ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dade8-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dade8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dade8-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dade8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dade8-105">DESCRIPTION</span></span>
<span data-ttu-id="dade8-106">**Yeni-AzureRmServerManagementGateway** cmdlet 'ı bir Azure Server yönetim ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="dade8-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="dade8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dade8-107">EXAMPLES</span></span>

## <span data-ttu-id="dade8-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dade8-108">PARAMETERS</span></span>

### <span data-ttu-id="dade8-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="dade8-109">-AutoUpgrade</span></span>
<span data-ttu-id="dade8-110">Yeni bir sürüm yayımlandığında ağ geçidinin otomatik olarak kendisini yükseltilecektir.</span><span class="sxs-lookup"><span data-stu-id="dade8-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dade8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dade8-111">-DefaultProfile</span></span>
<span data-ttu-id="dade8-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dade8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dade8-113">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="dade8-113">-GatewayName</span></span>
<span data-ttu-id="dade8-114">Bu cmdlet 'in oluşturduğu ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dade8-114">Specifies the name of the gateway that this cmdlet creates.</span></span>

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

### <span data-ttu-id="dade8-115">-Konum</span><span class="sxs-lookup"><span data-stu-id="dade8-115">-Location</span></span>
<span data-ttu-id="dade8-116">Ağ geçidinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dade8-116">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dade8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dade8-117">-ResourceGroupName</span></span>
<span data-ttu-id="dade8-118">Bu cmdlet 'in ağ geçidini oluşturduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dade8-118">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

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

### <span data-ttu-id="dade8-119">Etiketli</span><span class="sxs-lookup"><span data-stu-id="dade8-119">-Tag</span></span>
<span data-ttu-id="dade8-120">Ağ geçidiyle ilişkilendirilmiş anahtar/değer çiftleri.</span><span class="sxs-lookup"><span data-stu-id="dade8-120">Key/value pairs associated with the gateway.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dade8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dade8-121">CommonParameters</span></span>
<span data-ttu-id="dade8-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dade8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dade8-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dade8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dade8-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dade8-124">INPUTS</span></span>

### <span data-ttu-id="dade8-125">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dade8-125">None</span></span>
<span data-ttu-id="dade8-126">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="dade8-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dade8-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dade8-127">OUTPUTS</span></span>

### <span data-ttu-id="dade8-128">Microsoft. Azure. Commands. ServerManagement. model. geçit</span><span class="sxs-lookup"><span data-stu-id="dade8-128">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="dade8-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dade8-129">NOTES</span></span>

## <span data-ttu-id="dade8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dade8-130">RELATED LINKS</span></span>

[<span data-ttu-id="dade8-131">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="dade8-131">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="dade8-132">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="dade8-132">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


