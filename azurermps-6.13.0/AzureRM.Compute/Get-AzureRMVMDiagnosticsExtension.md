---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: fbc357decbf4bdcd2e378294fed43125d38fd873
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588576"
---
# <span data-ttu-id="7f734-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="7f734-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="7f734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f734-102">SYNOPSIS</span></span>
<span data-ttu-id="7f734-103">Sanal makinedeki tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="7f734-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f734-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7f734-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f734-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7f734-105">DESCRIPTION</span></span>
<span data-ttu-id="7f734-106">**Get-Azurermvmdiagnosticsextenter** cmdlet 'i, bir sanal makinedeki Azure tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="7f734-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="7f734-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7f734-107">EXAMPLES</span></span>

### <span data-ttu-id="7f734-108">Örnek 1: sanal makineye tanılama uzantısı uygulanır</span><span class="sxs-lookup"><span data-stu-id="7f734-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="7f734-109">Bu komut, ContosoVM22 adındaki sanal makineye uygulanan tanılama uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="7f734-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="7f734-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7f734-110">PARAMETERS</span></span>

### <span data-ttu-id="7f734-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f734-111">-DefaultProfile</span></span>
<span data-ttu-id="7f734-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7f734-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f734-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7f734-113">-Name</span></span>
<span data-ttu-id="7f734-114">Bu cmdlet 'in ayarları aldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f734-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f734-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f734-115">-ResourceGroupName</span></span>
<span data-ttu-id="7f734-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f734-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7f734-117">-Durum</span><span class="sxs-lookup"><span data-stu-id="7f734-117">-Status</span></span>
<span data-ttu-id="7f734-118">Bu cmdlet 'in durum değerini kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="7f734-118">Indicates that this cmdlet uses the Status value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f734-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="7f734-119">-VMName</span></span>
<span data-ttu-id="7f734-120">Bu cmdlet 'in tanılama uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7f734-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f734-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f734-121">CommonParameters</span></span>
<span data-ttu-id="7f734-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7f734-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f734-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f734-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f734-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7f734-124">INPUTS</span></span>

### <span data-ttu-id="7f734-125">System. String</span><span class="sxs-lookup"><span data-stu-id="7f734-125">System.String</span></span>

### <span data-ttu-id="7f734-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f734-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f734-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7f734-127">OUTPUTS</span></span>

### <span data-ttu-id="7f734-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="7f734-128">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="7f734-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7f734-129">NOTES</span></span>

## <span data-ttu-id="7f734-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7f734-130">RELATED LINKS</span></span>

[<span data-ttu-id="7f734-131">Remove-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="7f734-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="7f734-132">Set-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="7f734-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


