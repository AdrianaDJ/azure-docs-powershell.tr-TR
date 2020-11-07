---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 869167AA-54F8-4A1C-AC08-5555A63EE1BC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/get-azurermdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Get-AzureRmDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 25b3f15b6a71b54cbcab1a53f793a32da8b2173a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762534"
---
# <span data-ttu-id="df927-101">Get-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="df927-101">Get-AzureRmDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="df927-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df927-102">SYNOPSIS</span></span>
<span data-ttu-id="df927-103">DevTest laboratuvarlarında bir laboratuvarın izin verilen sanal makine boyutları ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="df927-103">Gets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df927-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df927-104">SYNTAX</span></span>

```
Get-AzureRmDtlAllowedVMSizesPolicy [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df927-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df927-105">DESCRIPTION</span></span>
<span data-ttu-id="df927-106">**Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet 'i, laboratuvarda izin verilen sanal makine boyutlarının listesini belirtmenize olanak sağlayan izin verilen sanal makine boyutları ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="df927-106">The **Get-AzureRmDtlAllowedVMSizesPolicy** cmdlet gets the allowed virtual machine sizes policy, which allows you to specify a list of virtual machine sizes allowed in the lab.</span></span>
<span data-ttu-id="df927-107">Cmdlet ilkenin etkin veya devre dışı durumunu ve belirtilen ilkede ayarlamış olduğunuz tüm izin verilen sanal makine boyutlarının listesini döndürür.</span><span class="sxs-lookup"><span data-stu-id="df927-107">The cmdlet returns the enabled or disabled status of the policy and a list of all the allowed virtual machine sizes that you have set in the specified policy.</span></span>

## <span data-ttu-id="df927-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df927-108">EXAMPLES</span></span>

## <span data-ttu-id="df927-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df927-109">PARAMETERS</span></span>

### <span data-ttu-id="df927-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df927-110">-DefaultProfile</span></span>
<span data-ttu-id="df927-111">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="df927-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df927-112">-LabName</span><span class="sxs-lookup"><span data-stu-id="df927-112">-LabName</span></span>
<span data-ttu-id="df927-113">Bu cmdlet 'in sanal makine boyutu ilkesini aldığı laboratuarın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df927-113">Specifies the name of the lab for which this cmdlet gets virtual machines size policy.</span></span>

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

### <span data-ttu-id="df927-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df927-114">-ResourceGroupName</span></span>
<span data-ttu-id="df927-115">Laboratuarın ait olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df927-115">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="df927-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df927-116">CommonParameters</span></span>
<span data-ttu-id="df927-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df927-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df927-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df927-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df927-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df927-119">INPUTS</span></span>

### <span data-ttu-id="df927-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="df927-120">None</span></span>
<span data-ttu-id="df927-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="df927-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df927-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df927-122">OUTPUTS</span></span>

### <span data-ttu-id="df927-123">Microsoft. Azure. Commands. DevTestLabs. model. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="df927-123">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>
<span data-ttu-id="df927-124">Bu cmdlet, laboratuvarda izin verilen sanal makine boyutlarının listesini belirten ilkeyi döndürür.</span><span class="sxs-lookup"><span data-stu-id="df927-124">This cmdlet returns the policy that specifies the list of virtual machine sizes allowed in the lab.</span></span>

## <span data-ttu-id="df927-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df927-125">NOTES</span></span>

## <span data-ttu-id="df927-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df927-126">RELATED LINKS</span></span>

[<span data-ttu-id="df927-127">Set-AzureRmDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="df927-127">Set-AzureRmDtlAllowedVMSizesPolicy</span></span>](./Set-AzureRmDtlAllowedVMSizesPolicy.md)

[<span data-ttu-id="df927-128">Azure geliştirme test laboratuarı cmdlet 'Leri</span><span class="sxs-lookup"><span data-stu-id="df927-128">Azure Development Test Lab Cmdlets</span></span>](./AzureRM.DevTestLabs.md)

