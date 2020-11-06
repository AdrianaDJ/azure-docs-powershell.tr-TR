---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 0ddfbd8aceeb26a4f40fcf104919fa9b67b39aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572969"
---
# <span data-ttu-id="00af9-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="00af9-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="00af9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00af9-102">SYNOPSIS</span></span>
<span data-ttu-id="00af9-103">Bir modülü otomatikleştirme 'ye aktarır.</span><span class="sxs-lookup"><span data-stu-id="00af9-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="00af9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="00af9-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00af9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="00af9-105">DESCRIPTION</span></span>
<span data-ttu-id="00af9-106">**Yeni-AzureRmAutomationModule** cmdlet 'ı Azure Otomasyonu 'nda modül içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="00af9-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="00af9-107">Bu komut,. zip dosya adı uzantısına sahip sıkıştırılmış bir dosyayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="00af9-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="00af9-108">Dosya, aşağıdaki türlerden birine sahip bir dosya içeren bir klasör içerir:</span><span class="sxs-lookup"><span data-stu-id="00af9-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="00af9-109">. psm1 veya. dll dosya adı uzantısına sahip wps_2 modülü</span><span class="sxs-lookup"><span data-stu-id="00af9-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="00af9-110">. psd1 dosya adı uzantısına sahip wps_2 modül bildirimi,. zip dosyasının adı, klasörün adı ve klasörün adı aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="00af9-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="00af9-111">. Zip dosyasını Otomasyon hizmetinin erişebileceği bir URL olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="00af9-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="00af9-112">Bu cmdlet veya Set-AzureRmAutomationModule cmdlet 'ini kullanarak bir wps_2 modülünü Otomasyonu</span><span class="sxs-lookup"><span data-stu-id="00af9-112">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="00af9-113">Bu komut almanın başarılı veya başarısız olduğunu sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="00af9-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="00af9-114">Başarılı olup olmadığını denetlemek için, aşağıdaki komutu çalıştırarak: `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name ` ModuleName başarılı bir şekilde **provisioningstate** özelliğini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="00af9-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="00af9-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="00af9-115">EXAMPLES</span></span>

### <span data-ttu-id="00af9-116">Örnek 1: modül Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="00af9-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="00af9-117">Bu komut, ContosoModule adlı bir modülü Contoso17 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="00af9-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="00af9-118">Modül, bir Azure Blob 'unda, contosostorage adlı bir depolama hesabında ve modüller adlı bir kapsayıcı içinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="00af9-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="00af9-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="00af9-119">PARAMETERS</span></span>

### <span data-ttu-id="00af9-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00af9-120">-AutomationAccountName</span></span>
<span data-ttu-id="00af9-121">Bu cmdlet 'in modül aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00af9-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="00af9-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="00af9-122">-ContentLinkUri</span></span>
<span data-ttu-id="00af9-123">Modül zip paketinin URL 'si</span><span class="sxs-lookup"><span data-stu-id="00af9-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="00af9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00af9-124">-DefaultProfile</span></span>
<span data-ttu-id="00af9-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="00af9-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00af9-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="00af9-126">-Name</span></span>
<span data-ttu-id="00af9-127">Bu cmdlet 'in içeri aktardığından modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00af9-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="00af9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00af9-128">-ResourceGroupName</span></span>
<span data-ttu-id="00af9-129">Bu cmdlet 'in modül aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="00af9-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="00af9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00af9-130">CommonParameters</span></span>
<span data-ttu-id="00af9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="00af9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00af9-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00af9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00af9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="00af9-133">INPUTS</span></span>

### <span data-ttu-id="00af9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="00af9-134">System.String</span></span>

### <span data-ttu-id="00af9-135">System. Uri</span><span class="sxs-lookup"><span data-stu-id="00af9-135">System.Uri</span></span>

## <span data-ttu-id="00af9-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="00af9-136">OUTPUTS</span></span>

### <span data-ttu-id="00af9-137">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="00af9-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="00af9-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="00af9-138">NOTES</span></span>

## <span data-ttu-id="00af9-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="00af9-139">RELATED LINKS</span></span>

[<span data-ttu-id="00af9-140">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="00af9-140">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="00af9-141">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="00af9-141">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="00af9-142">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="00af9-142">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


