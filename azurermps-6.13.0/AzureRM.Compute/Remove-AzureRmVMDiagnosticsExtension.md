---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMDiagnosticsExtension.md
ms.openlocfilehash: 4a14c5138a0dac983067e6deb4b1e05b88d85259
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593302"
---
# <span data-ttu-id="f92f6-101">Remove-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="f92f6-101">Remove-AzureRmVMDiagnosticsExtension</span></span>

## <span data-ttu-id="f92f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f92f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f92f6-103">Sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f92f6-103">Removes the Diagnostics extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f92f6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f92f6-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f92f6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f92f6-105">DESCRIPTION</span></span>
<span data-ttu-id="f92f6-106">**Remove-Azurermvmdiagnosticsextenma** cmdlet 'i, bir Azure Diagnostics uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f92f6-106">The **Remove-AzureRmVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="f92f6-107">Değişikliklerinizi uygulamak için bu cmdlet 'in çıkışını Update-AzureRmVM cmdlet 'ine geçirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f92f6-107">You must pass the output of this cmdlet to the Update-AzureRmVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="f92f6-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f92f6-108">EXAMPLES</span></span>

### <span data-ttu-id="f92f6-109">Örnek 1: sanal makineden tanılama uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="f92f6-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzureRmVM
```

<span data-ttu-id="f92f6-110">Bu komut, ContosoVM22 adındaki bir sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="f92f6-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="f92f6-111">Komut sonucu, ardışık düzen işlecini kullanarak Update-AzureRmVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="f92f6-111">The command passes the result to the Update-AzureRmVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f92f6-112">Bu komut sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f92f6-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="f92f6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f92f6-113">PARAMETERS</span></span>

### <span data-ttu-id="f92f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92f6-114">-DefaultProfile</span></span>
<span data-ttu-id="f92f6-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f92f6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f92f6-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="f92f6-116">-Name</span></span>
<span data-ttu-id="f92f6-117">Bu cmdlet 'in kaldırıldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f92f6-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f92f6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f92f6-118">-ResourceGroupName</span></span>
<span data-ttu-id="f92f6-119">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f92f6-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f92f6-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="f92f6-120">-VMName</span></span>
<span data-ttu-id="f92f6-121">Bu cmdlet 'in tanılama uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="f92f6-121">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="f92f6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92f6-122">CommonParameters</span></span>
<span data-ttu-id="f92f6-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f92f6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92f6-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f92f6-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92f6-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f92f6-125">INPUTS</span></span>

### <span data-ttu-id="f92f6-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f92f6-126">System.String</span></span>

## <span data-ttu-id="f92f6-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f92f6-127">OUTPUTS</span></span>

### <span data-ttu-id="f92f6-128">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f92f6-128">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="f92f6-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f92f6-129">NOTES</span></span>

## <span data-ttu-id="f92f6-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f92f6-130">RELATED LINKS</span></span>

[<span data-ttu-id="f92f6-131">Get-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="f92f6-131">Get-AzureRmVMDiagnosticsExtension</span></span>](./Get-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="f92f6-132">Set-azurermvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="f92f6-132">Set-AzureRmVMDiagnosticsExtension</span></span>](./Set-AzureRMVMDiagnosticsExtension.md)

[<span data-ttu-id="f92f6-133">Güncelleştirme-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="f92f6-133">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


