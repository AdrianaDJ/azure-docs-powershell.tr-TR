---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bcfc7f3d80c5601d5797d9af2958d2bed6395fbe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917300"
---
# <span data-ttu-id="e4c9f-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="e4c9f-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="e4c9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c9f-103">Sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="e4c9f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4c9f-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4c9f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4c9f-105">DESCRIPTION</span></span>
<span data-ttu-id="e4c9f-106">**Remove-Azvmdiagnosticsextenkomutçuğu** , bir Azure Diagnostics uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="e4c9f-107">Değişikliklerinizi uygulamak için bu cmdlet 'in çıkışını Update-AzVM cmdlet 'ine geçirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="e4c9f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4c9f-108">EXAMPLES</span></span>

### <span data-ttu-id="e4c9f-109">Örnek 1: sanal makineden tanılama uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="e4c9f-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="e4c9f-110">Bu komut, ContosoVM22 adındaki bir sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="e4c9f-111">Komut sonucu, ardışık düzen işlecini kullanarak Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e4c9f-112">Bu komut sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="e4c9f-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4c9f-113">PARAMETERS</span></span>

### <span data-ttu-id="e4c9f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c9f-114">-DefaultProfile</span></span>
<span data-ttu-id="e4c9f-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4c9f-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4c9f-116">-Name</span></span>
<span data-ttu-id="e4c9f-117">Bu cmdlet 'in kaldırıldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e4c9f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c9f-118">-ResourceGroupName</span></span>
<span data-ttu-id="e4c9f-119">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e4c9f-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="e4c9f-120">-VMName</span></span>
<span data-ttu-id="e4c9f-121">Bu cmdlet 'in tanılama uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="e4c9f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c9f-122">CommonParameters</span></span>
<span data-ttu-id="e4c9f-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4c9f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c9f-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4c9f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c9f-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4c9f-125">INPUTS</span></span>

### <span data-ttu-id="e4c9f-126">System. String</span><span class="sxs-lookup"><span data-stu-id="e4c9f-126">System.String</span></span>

## <span data-ttu-id="e4c9f-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4c9f-127">OUTPUTS</span></span>

### <span data-ttu-id="e4c9f-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e4c9f-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e4c9f-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4c9f-129">NOTES</span></span>

## <span data-ttu-id="e4c9f-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4c9f-130">RELATED LINKS</span></span>

[<span data-ttu-id="e4c9f-131">Get-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="e4c9f-131">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="e4c9f-132">Set-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="e4c9f-132">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="e4c9f-133">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="e4c9f-133">Update-AzVM</span></span>](./Update-AzVM.md)


