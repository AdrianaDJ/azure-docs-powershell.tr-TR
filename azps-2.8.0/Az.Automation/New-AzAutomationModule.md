---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: 7e9b2e9a87cc9a02c807a2eae3b64e7a13c87a1b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753277"
---
# <span data-ttu-id="fba4e-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fba4e-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="fba4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fba4e-102">SYNOPSIS</span></span>
<span data-ttu-id="fba4e-103">Bir modülü otomatikleştirme 'ye aktarır.</span><span class="sxs-lookup"><span data-stu-id="fba4e-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="fba4e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fba4e-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fba4e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fba4e-105">DESCRIPTION</span></span>
<span data-ttu-id="fba4e-106">**New-AzAutomationModule** cmdlet 'ı Azure Otomasyonu 'nda modül içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="fba4e-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="fba4e-107">Bu komut,. zip dosya adı uzantısına sahip sıkıştırılmış bir dosyayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="fba4e-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="fba4e-108">Dosya, aşağıdaki türlerden birine sahip bir dosya içeren bir klasör içerir:</span><span class="sxs-lookup"><span data-stu-id="fba4e-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="fba4e-109">. Psm1 veya. dll dosya adı uzantısına sahip Windows PowerShell modülü</span><span class="sxs-lookup"><span data-stu-id="fba4e-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="fba4e-110">. Psd1 dosya adı uzantısına sahip Windows PowerShell modülü bildirimi. zip dosyasının adı, klasörün adı ve klasörün adı aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="fba4e-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="fba4e-111">. Zip dosyasını Otomasyon hizmetinin erişebileceği bir URL olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="fba4e-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="fba4e-112">Windows PowerShell modülünü bu cmdlet 'i veya Set-AzAutomationModule cmdlet 'ini kullanarak Otomasyon 'a aktarırsanız, işlem zaman uyumsuzdur.</span><span class="sxs-lookup"><span data-stu-id="fba4e-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="fba4e-113">Bu komut almanın başarılı veya başarısız olduğunu sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="fba4e-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="fba4e-114">Başarılı olup olmadığını denetlemek için, aşağıdaki komutu çalıştırarak: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName başarılı bir şekilde **provisioningstate** özelliğini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="fba4e-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="fba4e-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fba4e-115">EXAMPLES</span></span>

### <span data-ttu-id="fba4e-116">Örnek 1: modül Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="fba4e-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fba4e-117">Bu komut, ContosoModule adlı bir modülü Contoso17 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="fba4e-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="fba4e-118">Modül, bir Azure Blob 'unda, contosostorage adlı bir depolama hesabında ve modüller adlı bir kapsayıcı içinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="fba4e-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="fba4e-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fba4e-119">PARAMETERS</span></span>

### <span data-ttu-id="fba4e-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fba4e-120">-AutomationAccountName</span></span>
<span data-ttu-id="fba4e-121">Bu cmdlet 'in modül aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba4e-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="fba4e-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="fba4e-122">-ContentLinkUri</span></span>
<span data-ttu-id="fba4e-123">Modül zip paketinin URL 'si</span><span class="sxs-lookup"><span data-stu-id="fba4e-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fba4e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fba4e-124">-DefaultProfile</span></span>
<span data-ttu-id="fba4e-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fba4e-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fba4e-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="fba4e-126">-Name</span></span>
<span data-ttu-id="fba4e-127">Bu cmdlet 'in içeri aktardığından modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba4e-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="fba4e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fba4e-128">-ResourceGroupName</span></span>
<span data-ttu-id="fba4e-129">Bu cmdlet 'in modül aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fba4e-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="fba4e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fba4e-130">CommonParameters</span></span>
<span data-ttu-id="fba4e-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fba4e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fba4e-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fba4e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fba4e-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fba4e-133">INPUTS</span></span>

### <span data-ttu-id="fba4e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="fba4e-134">System.String</span></span>

### <span data-ttu-id="fba4e-135">System. Uri</span><span class="sxs-lookup"><span data-stu-id="fba4e-135">System.Uri</span></span>

## <span data-ttu-id="fba4e-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fba4e-136">OUTPUTS</span></span>

### <span data-ttu-id="fba4e-137">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="fba4e-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="fba4e-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fba4e-138">NOTES</span></span>

## <span data-ttu-id="fba4e-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fba4e-139">RELATED LINKS</span></span>

[<span data-ttu-id="fba4e-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fba4e-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="fba4e-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fba4e-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="fba4e-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="fba4e-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


