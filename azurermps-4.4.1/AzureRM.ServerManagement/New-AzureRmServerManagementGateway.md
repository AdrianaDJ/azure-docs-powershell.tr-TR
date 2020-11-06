---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: D7485CB9-AE12-445B-8984-3D21FCA0E82F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/New-AzureRmServerManagementGateway.md
ms.openlocfilehash: 9cb98b9671f43ddd7acbcc84e8473a12da00f405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93590636"
---
# <span data-ttu-id="cb323-101">New-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="cb323-101">New-AzureRmServerManagementGateway</span></span>

## <span data-ttu-id="cb323-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cb323-102">SYNOPSIS</span></span>
<span data-ttu-id="cb323-103">Sunucu yönetimi ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb323-103">Creates a Server Management gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb323-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cb323-104">SYNTAX</span></span>

```
New-AzureRmServerManagementGateway [-ResourceGroupName] <String> [-GatewayName] <String> [-Location] <String>
 [-AutoUpgrade] [-Tags <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb323-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cb323-105">DESCRIPTION</span></span>
<span data-ttu-id="cb323-106">**Yeni-AzureRmServerManagementGateway** cmdlet 'ı bir Azure Server yönetim ağ geçidi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cb323-106">The **New-AzureRmServerManagementGateway** cmdlet creates an Azure Server Management gateway.</span></span>

## <span data-ttu-id="cb323-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cb323-107">EXAMPLES</span></span>

## <span data-ttu-id="cb323-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cb323-108">PARAMETERS</span></span>

### <span data-ttu-id="cb323-109">-AutoUpgrade</span><span class="sxs-lookup"><span data-stu-id="cb323-109">-AutoUpgrade</span></span>
<span data-ttu-id="cb323-110">Yeni bir sürüm yayımlandığında ağ geçidinin otomatik olarak kendisini yükseltilecektir.</span><span class="sxs-lookup"><span data-stu-id="cb323-110">Indicates that the gateway will auto upgrade itself when a new version is released.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb323-111">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="cb323-111">-GatewayName</span></span>
<span data-ttu-id="cb323-112">Bu cmdlet 'in oluşturduğu ağ geçidinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb323-112">Specifies the name of the gateway that this cmdlet creates.</span></span>

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

### <span data-ttu-id="cb323-113">-Konum</span><span class="sxs-lookup"><span data-stu-id="cb323-113">-Location</span></span>
<span data-ttu-id="cb323-114">Ağ geçidinin oluşturulacağı konumu belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb323-114">Specifies the location in which to create the gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb323-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb323-115">-ResourceGroupName</span></span>
<span data-ttu-id="cb323-116">Bu cmdlet 'in ağ geçidini oluşturduğu kaynak grubun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb323-116">Specifies the name of the resource group in which this cmdlet creates the gateway.</span></span>

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

### <span data-ttu-id="cb323-117">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="cb323-117">-Tags</span></span>
<span data-ttu-id="cb323-118">Etiketleri anahtar-değer çiftleri olarak belirtir.</span><span class="sxs-lookup"><span data-stu-id="cb323-118">Specifies tags as key-value pairs.</span></span>
<span data-ttu-id="cb323-119">Diğer Azure kaynaklarından gelen bir ağ geçidini belirlemek için Etiketler 'i kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="cb323-119">You can use tags to identify a Gateway from other Azure resources.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb323-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb323-120">-DefaultProfile</span></span>
<span data-ttu-id="cb323-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="cb323-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb323-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb323-122">CommonParameters</span></span>
<span data-ttu-id="cb323-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cb323-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb323-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb323-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb323-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cb323-125">INPUTS</span></span>

## <span data-ttu-id="cb323-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cb323-126">OUTPUTS</span></span>

### <span data-ttu-id="cb323-127">Microsoft. Azure. Commands. ServerManagement. model. geçit</span><span class="sxs-lookup"><span data-stu-id="cb323-127">Microsoft.Azure.Commands.ServerManagement.Model.Gateway</span></span>

## <span data-ttu-id="cb323-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cb323-128">NOTES</span></span>

## <span data-ttu-id="cb323-129">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cb323-129">RELATED LINKS</span></span>

[<span data-ttu-id="cb323-130">Get-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="cb323-130">Get-AzureRmServerManagementGateway</span></span>](./Get-AzureRmServerManagementGateway.md)

[<span data-ttu-id="cb323-131">Remove-AzureRmServerManagementGateway</span><span class="sxs-lookup"><span data-stu-id="cb323-131">Remove-AzureRmServerManagementGateway</span></span>](./Remove-AzureRmServerManagementGateway.md)


