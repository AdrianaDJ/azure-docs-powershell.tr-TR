---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 91adec21cd620b0ac126a91191dba7ccdf0b3767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762176"
---
# <span data-ttu-id="9afd4-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9afd4-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="9afd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9afd4-102">SYNOPSIS</span></span>
<span data-ttu-id="9afd4-103">Bir modülü otomatikleştirme 'ye aktarır.</span><span class="sxs-lookup"><span data-stu-id="9afd4-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9afd4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9afd4-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9afd4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9afd4-105">DESCRIPTION</span></span>
<span data-ttu-id="9afd4-106">**Yeni-AzureRmAutomationModule** cmdlet 'ı Azure Otomasyonu 'nda modül içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="9afd4-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="9afd4-107">Bu komut,. zip dosya adı uzantısına sahip sıkıştırılmış bir dosyayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="9afd4-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="9afd4-108">Dosya, aşağıdaki türlerden birine sahip bir dosya içeren bir klasör içerir:</span><span class="sxs-lookup"><span data-stu-id="9afd4-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="9afd4-109">. psm1 veya. dll dosya adı uzantısına sahip wps_2 modülü</span><span class="sxs-lookup"><span data-stu-id="9afd4-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="9afd4-110">. psd1 dosya adı uzantısına sahip wps_2 modül bildirimi</span><span class="sxs-lookup"><span data-stu-id="9afd4-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="9afd4-111">. Zip dosyasının adı, klasörün adı ve klasörün adı, aynı olmalıdır. "</span><span class="sxs-lookup"><span data-stu-id="9afd4-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="9afd4-112">. Zip dosyasını Otomasyon hizmetinin erişebileceği bir URL olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="9afd4-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="9afd4-113">Bu cmdlet veya Set-AzureRmAutomationModule cmdlet 'ini kullanarak bir wps_2 modülünü Otomasyonu</span><span class="sxs-lookup"><span data-stu-id="9afd4-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="9afd4-114">Bu komut almanın başarılı veya başarısız olduğunu sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="9afd4-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="9afd4-115">Başarılı olup olmadığını denetlemek için aşağıdaki komutu deneyin:</span><span class="sxs-lookup"><span data-stu-id="9afd4-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="9afd4-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `Ladı</span><span class="sxs-lookup"><span data-stu-id="9afd4-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="9afd4-117">Başarılı bir değer için **Provisioningstate** özelliğini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="9afd4-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="9afd4-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9afd4-118">EXAMPLES</span></span>

### <span data-ttu-id="9afd4-119">Örnek 1: modül Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="9afd4-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="9afd4-120">Bu komut, ContosoModule adlı bir modülü Contoso17 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="9afd4-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="9afd4-121">Modül, bir Azure Blob 'unda, contosostorage adlı bir depolama hesabında ve modüller adlı bir kapsayıcı içinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="9afd4-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="9afd4-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9afd4-122">PARAMETERS</span></span>

### <span data-ttu-id="9afd4-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9afd4-123">-AutomationAccountName</span></span>
<span data-ttu-id="9afd4-124">Bu cmdlet 'in modül aldığı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9afd4-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="9afd4-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="9afd4-125">-ContentLinkUri</span></span>
<span data-ttu-id="9afd4-126">Modül zip paketinin URL 'si</span><span class="sxs-lookup"><span data-stu-id="9afd4-126">The url to a module zip package</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9afd4-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9afd4-127">-DefaultProfile</span></span>
<span data-ttu-id="9afd4-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="9afd4-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9afd4-129">-Ad</span><span class="sxs-lookup"><span data-stu-id="9afd4-129">-Name</span></span>
<span data-ttu-id="9afd4-130">Bu cmdlet 'in içeri aktardığından modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9afd4-130">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9afd4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9afd4-131">-ResourceGroupName</span></span>
<span data-ttu-id="9afd4-132">Bu cmdlet 'in modül aldığı kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9afd4-132">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="9afd4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9afd4-133">CommonParameters</span></span>
<span data-ttu-id="9afd4-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9afd4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9afd4-135">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9afd4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9afd4-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9afd4-136">INPUTS</span></span>

### <span data-ttu-id="9afd4-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9afd4-137">None</span></span>
<span data-ttu-id="9afd4-138">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9afd4-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9afd4-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9afd4-139">OUTPUTS</span></span>

### <span data-ttu-id="9afd4-140">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="9afd4-140">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="9afd4-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9afd4-141">NOTES</span></span>

## <span data-ttu-id="9afd4-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9afd4-142">RELATED LINKS</span></span>

[<span data-ttu-id="9afd4-143">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9afd4-143">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="9afd4-144">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9afd4-144">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="9afd4-145">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="9afd4-145">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


