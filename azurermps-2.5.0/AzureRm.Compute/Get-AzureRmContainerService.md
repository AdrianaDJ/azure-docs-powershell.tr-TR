---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 5db21871b84801d57deebf98e27bbe153285631a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940193"
---
# <span data-ttu-id="36f28-101">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="36f28-101">Get-AzureRmContainerService</span></span>

## <span data-ttu-id="36f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36f28-102">SYNOPSIS</span></span>
<span data-ttu-id="36f28-103">Kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="36f28-103">Gets a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36f28-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="36f28-104">SYNTAX</span></span>

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36f28-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="36f28-105">DESCRIPTION</span></span>
<span data-ttu-id="36f28-106">**Get-AzureRmContainerService** cmdlet 'i bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="36f28-106">The **Get-AzureRmContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="36f28-107">Ana ve aracının tam nitelikli etki alanı adını içeren, bölge, ana ve aracılar sayısı gibi bir kapsayıcı hizmetin özelliklerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="36f28-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="36f28-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="36f28-108">EXAMPLES</span></span>

### <span data-ttu-id="36f28-109">Örnek 1: kapsayıcı hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="36f28-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="36f28-110">Bu komut, CSResourceGroup17 adlı bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="36f28-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="36f28-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="36f28-111">PARAMETERS</span></span>

### <span data-ttu-id="36f28-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f28-112">-DefaultProfile</span></span>
<span data-ttu-id="36f28-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="36f28-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="36f28-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="36f28-114">-Name</span></span>
<span data-ttu-id="36f28-115">Bu cmdlet 'in aldığı kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f28-115">Specifies the name of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f28-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f28-116">-ResourceGroupName</span></span>
<span data-ttu-id="36f28-117">Bu cmdlet 'in aldığı kapsayıcı hizmetinin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="36f28-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f28-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f28-118">CommonParameters</span></span>
<span data-ttu-id="36f28-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="36f28-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f28-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f28-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f28-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="36f28-121">INPUTS</span></span>

### <span data-ttu-id="36f28-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="36f28-122">None</span></span>
<span data-ttu-id="36f28-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="36f28-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36f28-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="36f28-124">OUTPUTS</span></span>

### <span data-ttu-id="36f28-125">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="36f28-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="36f28-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="36f28-126">NOTES</span></span>

## <span data-ttu-id="36f28-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="36f28-127">RELATED LINKS</span></span>

[<span data-ttu-id="36f28-128">Yeni-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="36f28-128">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="36f28-129">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="36f28-129">Remove-AzureRmContainerService</span></span>](./Remove-AzureRmContainerService.md)

[<span data-ttu-id="36f28-130">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="36f28-130">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


