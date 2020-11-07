---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: bec83334032b3d0e18c017bc24d19d381a765176
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936911"
---
# <span data-ttu-id="c9ce8-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c9ce8-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="c9ce8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9ce8-102">SYNOPSIS</span></span>
<span data-ttu-id="c9ce8-103">Sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="c9ce8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c9ce8-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9ce8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c9ce8-105">DESCRIPTION</span></span>
<span data-ttu-id="c9ce8-106">**Remove-Azvmdiagnosticsextenkomutçuğu** , bir Azure Diagnostics uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="c9ce8-107">Değişikliklerinizi uygulamak için bu cmdlet 'in çıkışını Update-AzVM cmdlet 'ine geçirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="c9ce8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c9ce8-108">EXAMPLES</span></span>

### <span data-ttu-id="c9ce8-109">Örnek 1: sanal makineden tanılama uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="c9ce8-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="c9ce8-110">Bu komut, ContosoVM22 adındaki bir sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="c9ce8-111">Komut sonucu, ardışık düzen işlecini kullanarak Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="c9ce8-112">Bu komut sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="c9ce8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c9ce8-113">PARAMETERS</span></span>

### <span data-ttu-id="c9ce8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9ce8-114">-DefaultProfile</span></span>
<span data-ttu-id="c9ce8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9ce8-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="c9ce8-116">-Name</span></span>
<span data-ttu-id="c9ce8-117">Bu cmdlet 'in kaldırıldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9ce8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9ce8-118">-ResourceGroupName</span></span>
<span data-ttu-id="c9ce8-119">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c9ce8-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="c9ce8-120">-VMName</span></span>
<span data-ttu-id="c9ce8-121">Bu cmdlet 'in tanılama uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9ce8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9ce8-122">CommonParameters</span></span>
<span data-ttu-id="c9ce8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9ce8-124">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9ce8-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9ce8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c9ce8-125">INPUTS</span></span>

### <span data-ttu-id="c9ce8-126">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="c9ce8-126">None</span></span>
<span data-ttu-id="c9ce8-127">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="c9ce8-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9ce8-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c9ce8-128">OUTPUTS</span></span>

### <span data-ttu-id="c9ce8-129">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c9ce8-129">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="c9ce8-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c9ce8-130">NOTES</span></span>

## <span data-ttu-id="c9ce8-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c9ce8-131">RELATED LINKS</span></span>

[<span data-ttu-id="c9ce8-132">Get-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="c9ce8-132">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="c9ce8-133">Set-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="c9ce8-133">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="c9ce8-134">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="c9ce8-134">Update-AzVM</span></span>](./Update-AzVM.md)


