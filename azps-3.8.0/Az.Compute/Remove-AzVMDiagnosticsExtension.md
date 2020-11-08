---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 89DA3965-5344-4A1D-AEF1-10EA58E129CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiagnosticsExtension.md
ms.openlocfilehash: 991b33bed897b0d33d9e5e0125dd7d9309f55bcd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097582"
---
# <span data-ttu-id="61f93-101">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="61f93-101">Remove-AzVMDiagnosticsExtension</span></span>

## <span data-ttu-id="61f93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f93-102">SYNOPSIS</span></span>
<span data-ttu-id="61f93-103">Sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61f93-103">Removes the Diagnostics extension from a virtual machine.</span></span>

## <span data-ttu-id="61f93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="61f93-104">SYNTAX</span></span>

```
Remove-AzVMDiagnosticsExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61f93-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="61f93-105">DESCRIPTION</span></span>
<span data-ttu-id="61f93-106">**Remove-Azvmdiagnosticsextenkomutçuğu** , bir Azure Diagnostics uzantısını sanal makineden kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61f93-106">The **Remove-AzVMDiagnosticsExtension** cmdlet removes an Azure Diagnostics extension from a virtual machine.</span></span>
<span data-ttu-id="61f93-107">Değişikliklerinizi uygulamak için bu cmdlet 'in çıkışını Update-AzVM cmdlet 'ine geçirmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="61f93-107">You must pass the output of this cmdlet to the Update-AzVM cmdlet to implement your changes.</span></span>

## <span data-ttu-id="61f93-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="61f93-108">EXAMPLES</span></span>

### <span data-ttu-id="61f93-109">Örnek 1: sanal makineden tanılama uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="61f93-109">Example 1: Remove the Diagnostics extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMDiagnosticsExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" | Update-AzVM
```

<span data-ttu-id="61f93-110">Bu komut, ContosoVM22 adındaki bir sanal makineden tanılama uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="61f93-110">This command removes the Diagnostics extension from a virtual machine named ContosoVM22.</span></span>
<span data-ttu-id="61f93-111">Komut sonucu, ardışık düzen işlecini kullanarak Update-AzVM cmdlet 'ine geçirir.</span><span class="sxs-lookup"><span data-stu-id="61f93-111">The command passes the result to the Update-AzVM cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="61f93-112">Bu komut sanal makineyi güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="61f93-112">That command updates the virtual machine.</span></span>

## <span data-ttu-id="61f93-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="61f93-113">PARAMETERS</span></span>

### <span data-ttu-id="61f93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f93-114">-DefaultProfile</span></span>
<span data-ttu-id="61f93-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="61f93-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61f93-116">-Ad</span><span class="sxs-lookup"><span data-stu-id="61f93-116">-Name</span></span>
<span data-ttu-id="61f93-117">Bu cmdlet 'in kaldırıldığı tanılama uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f93-117">Specifies the name of the Diagnostics extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="61f93-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="61f93-118">-NoWait</span></span>
<span data-ttu-id="61f93-119">İşlemi başlatır ve işlem tamamlanmadan hemen döner.</span><span class="sxs-lookup"><span data-stu-id="61f93-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="61f93-120">İşlemin başarıyla tamamlanıp tamamlanmadığını belirlemek için başka bir mekanizma kullanın.</span><span class="sxs-lookup"><span data-stu-id="61f93-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f93-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f93-121">-ResourceGroupName</span></span>
<span data-ttu-id="61f93-122">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f93-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="61f93-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="61f93-123">-VMName</span></span>
<span data-ttu-id="61f93-124">Bu cmdlet 'in tanılama uzantısını kaldırdığı sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="61f93-124">Specifies the name of the virtual machine from which this cmdlet removes a Diagnostics extension.</span></span>

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

### <span data-ttu-id="61f93-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f93-125">CommonParameters</span></span>
<span data-ttu-id="61f93-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="61f93-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f93-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="61f93-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f93-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="61f93-128">INPUTS</span></span>

### <span data-ttu-id="61f93-129">System. String</span><span class="sxs-lookup"><span data-stu-id="61f93-129">System.String</span></span>

## <span data-ttu-id="61f93-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="61f93-130">OUTPUTS</span></span>

### <span data-ttu-id="61f93-131">Microsoft. Azure. Commands. COMPUTE. modeller. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="61f93-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="61f93-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="61f93-132">NOTES</span></span>

## <span data-ttu-id="61f93-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="61f93-133">RELATED LINKS</span></span>

[<span data-ttu-id="61f93-134">Get-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="61f93-134">Get-AzVMDiagnosticsExtension</span></span>](./Get-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="61f93-135">Set-azvmdiagnosticsexten</span><span class="sxs-lookup"><span data-stu-id="61f93-135">Set-AzVMDiagnosticsExtension</span></span>](./Set-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="61f93-136">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="61f93-136">Update-AzVM</span></span>](./Update-AzVM.md)


