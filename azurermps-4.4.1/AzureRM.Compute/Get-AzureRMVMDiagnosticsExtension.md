---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5BEA683-44AE-4D71-827D-02A03F0BEAE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMDiagnosticsExtension.md
ms.openlocfilehash: fd401aa80f65888bc0540bb7975263108e0f8637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762281"
---
# <span data-ttu-id="e8063-101">Get-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e8063-101">Get-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="e8063-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8063-102">SYNOPSIS</span></span>
<span data-ttu-id="e8063-103">Sanal makinedeki tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e8063-103">Gets the settings of the Diagnostics extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8063-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8063-104">SYNTAX</span></span>

```
Get-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8063-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8063-105">DESCRIPTION</span></span>
<span data-ttu-id="e8063-106">**Get-Azurermvmdiagnosticsextenter** cmdlet 'i, bir sanal makinedeki Azure tanılama uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="e8063-106">The **Get-AzureRmVMDiagnosticsExtension** cmdlet gets the settings of the Azure Diagnostics extension on a virtual machine.</span></span>

## <span data-ttu-id="e8063-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8063-107">EXAMPLES</span></span>

### <span data-ttu-id="e8063-108">Örnek 1: sanal makineye tanılama uzantısı uygulanır</span><span class="sxs-lookup"><span data-stu-id="e8063-108">Example 1: Get the diagnostics extension applied to a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22"
```

<span data-ttu-id="e8063-109">Bu komut, ContosoVM22 adındaki sanal makineye uygulanan tanılama uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="e8063-109">This command gets the diagnostics extension applied to the virtual machine named ContosoVM22.</span></span>

## <span data-ttu-id="e8063-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8063-110">PARAMETERS</span></span>

### <span data-ttu-id="e8063-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8063-111">-DefaultProfile</span></span>
<span data-ttu-id="e8063-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8063-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8063-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8063-113">-Name</span></span>
<span data-ttu-id="e8063-114">Bu cmdlet 'in ayarları aldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8063-114">Specifies the name of the Diagnostics extension for which this cmdlet gets settings.</span></span>

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

### <span data-ttu-id="e8063-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8063-115">-ResourceGroupName</span></span>
<span data-ttu-id="e8063-116">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8063-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e8063-117">-Durum</span><span class="sxs-lookup"><span data-stu-id="e8063-117">-Status</span></span>
<span data-ttu-id="e8063-118">Bu cmdlet 'in durum değerini kullandığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8063-118">Indicates that this cmdlet uses the Status value.</span></span>

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

### <span data-ttu-id="e8063-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="e8063-119">-VMName</span></span>
<span data-ttu-id="e8063-120">Bu cmdlet 'in tanılama uzantısını aldığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e8063-120">Specifies the name of the virtual machine from which this cmdlet gets the Diagnostics extension.</span></span>

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

### <span data-ttu-id="e8063-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8063-121">CommonParameters</span></span>
<span data-ttu-id="e8063-122">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8063-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8063-123">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8063-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8063-124">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8063-124">INPUTS</span></span>

## <span data-ttu-id="e8063-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8063-125">OUTPUTS</span></span>

## <span data-ttu-id="e8063-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8063-126">NOTES</span></span>

## <span data-ttu-id="e8063-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8063-127">RELATED LINKS</span></span>

[<span data-ttu-id="e8063-128">Remove-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="e8063-128">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="e8063-129">Set-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="e8063-129">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)


