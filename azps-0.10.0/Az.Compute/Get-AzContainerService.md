---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzContainerService.md
ms.openlocfilehash: 1a0daa4bf336ba970c12c24db3d5aab73641aaea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937055"
---
# <span data-ttu-id="daae0-101">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="daae0-101">Get-AzContainerService</span></span>

## <span data-ttu-id="daae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daae0-102">SYNOPSIS</span></span>
<span data-ttu-id="daae0-103">Kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="daae0-103">Gets a container service.</span></span>

## <span data-ttu-id="daae0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="daae0-104">SYNTAX</span></span>

```
Get-AzContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="daae0-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="daae0-105">DESCRIPTION</span></span>
<span data-ttu-id="daae0-106">**Get-AzContainerService** cmdlet 'i bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="daae0-106">The **Get-AzContainerService** cmdlet gets a container service.</span></span>
<span data-ttu-id="daae0-107">Ana ve aracının tam nitelikli etki alanı adını içeren, bölge, ana ve aracılar sayısı gibi bir kapsayıcı hizmetin özelliklerini görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="daae0-107">You can view the properties of a container service, which include state, number of master and agents, and fully qualified domain name of master and agent.</span></span>

## <span data-ttu-id="daae0-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="daae0-108">EXAMPLES</span></span>

### <span data-ttu-id="daae0-109">Örnek 1: kapsayıcı hizmeti alma</span><span class="sxs-lookup"><span data-stu-id="daae0-109">Example 1: Get a container service</span></span>
```
PS C:\> Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="daae0-110">Bu komut, CSResourceGroup17 adlı bir kapsayıcı hizmeti alır.</span><span class="sxs-lookup"><span data-stu-id="daae0-110">This command gets a container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="daae0-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="daae0-111">PARAMETERS</span></span>

### <span data-ttu-id="daae0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daae0-112">-DefaultProfile</span></span>
<span data-ttu-id="daae0-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="daae0-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="daae0-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="daae0-114">-Name</span></span>
<span data-ttu-id="daae0-115">Bu cmdlet 'in aldığı kapsayıcı hizmetin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="daae0-115">Specifies the name of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="daae0-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daae0-116">-ResourceGroupName</span></span>
<span data-ttu-id="daae0-117">Bu cmdlet 'in aldığı kapsayıcı hizmetinin kaynak grubunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="daae0-117">Specifies the resource group of the container service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="daae0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daae0-118">CommonParameters</span></span>
<span data-ttu-id="daae0-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="daae0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daae0-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daae0-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daae0-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="daae0-121">INPUTS</span></span>

### <span data-ttu-id="daae0-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="daae0-122">None</span></span>
<span data-ttu-id="daae0-123">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="daae0-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="daae0-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="daae0-124">OUTPUTS</span></span>

### <span data-ttu-id="daae0-125">Microsoft. Azure. Commands. COMPUTE. Automation. modeller. PSContainerService</span><span class="sxs-lookup"><span data-stu-id="daae0-125">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="daae0-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="daae0-126">NOTES</span></span>

## <span data-ttu-id="daae0-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="daae0-127">RELATED LINKS</span></span>

[<span data-ttu-id="daae0-128">Yeni-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="daae0-128">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="daae0-129">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="daae0-129">Remove-AzContainerService</span></span>](./Remove-AzContainerService.md)

[<span data-ttu-id="daae0-130">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="daae0-130">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


