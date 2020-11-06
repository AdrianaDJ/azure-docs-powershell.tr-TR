---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: 7bec79c2c2c4bdc794b1d3b260cad53d82fa5d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593750"
---
# <span data-ttu-id="df267-101">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="df267-101">Set-AzureRmAutomationModule</span></span>

## <span data-ttu-id="df267-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df267-102">SYNOPSIS</span></span>
<span data-ttu-id="df267-103">Otomasyon 'da bir modülü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="df267-103">Updates a module in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df267-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="df267-104">SYNTAX</span></span>

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="df267-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="df267-105">DESCRIPTION</span></span>
<span data-ttu-id="df267-106">**Set-AzureRmAutomationModule** cmdlet 'ı Azure Otomasyonu 'nda bir modülü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="df267-106">The **Set-AzureRmAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="df267-107">Bu komut,. zip dosya adı uzantısına sahip sıkıştırılmış bir dosyayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="df267-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="df267-108">Dosya, aşağıdaki türlerden birine sahip bir dosya içeren bir klasör içerir:</span><span class="sxs-lookup"><span data-stu-id="df267-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="df267-109">. psm1 veya. dll dosya adı uzantısına sahip wps_2 modülü</span><span class="sxs-lookup"><span data-stu-id="df267-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="df267-110">. psd1 dosya adı uzantısına sahip wps_2 modül bildirimi</span><span class="sxs-lookup"><span data-stu-id="df267-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="df267-111">. Zip dosyasının adı, klasörün adı ve klasörün adı, aynı olmalıdır. "</span><span class="sxs-lookup"><span data-stu-id="df267-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="df267-112">. Zip dosyasını Otomasyon hizmetinin erişebileceği bir URL olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="df267-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="df267-113">Bu cmdlet veya New-AzureRmAutomationModule cmdlet 'ini kullanarak bir wps_2 modülünü Otomasyonu</span><span class="sxs-lookup"><span data-stu-id="df267-113">If you import a wps_2 module into Automation by using this cmdlet or the New-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="df267-114">Bu komut almanın başarılı veya başarısız olduğunu sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="df267-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="df267-115">Başarılı olup olmadığını denetlemek için aşağıdaki komutu deneyin:</span><span class="sxs-lookup"><span data-stu-id="df267-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="df267-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `Ladı</span><span class="sxs-lookup"><span data-stu-id="df267-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="df267-117">Başarılı bir değer için **Provisioningstate** özelliğini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="df267-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="df267-118">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="df267-118">EXAMPLES</span></span>

### <span data-ttu-id="df267-119">Örnek 1: modül güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="df267-119">Example 1: Update a module</span></span>
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="df267-120">Bu komut, Contoso17 adlı Otomasyon hesabına ContosoModule adlı var olan bir modülün güncelleştirilmiş sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="df267-120">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="df267-121">Modül, bir Azure Blob 'unda, contosostorage adlı bir depolama hesabında ve modüller adlı bir kapsayıcı içinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="df267-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="df267-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="df267-122">PARAMETERS</span></span>

### <span data-ttu-id="df267-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="df267-123">-AutomationAccountName</span></span>
<span data-ttu-id="df267-124">Bu cmdlet 'in modülü güncelleştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df267-124">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="df267-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="df267-125">-ContentLinkUri</span></span>
<span data-ttu-id="df267-126">Bu cmdlet 'in içeri aktardığından, modülün yeni sürümünü içeren. zip dosyasının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="df267-126">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df267-127">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="df267-127">-ContentLinkVersion</span></span>
<span data-ttu-id="df267-128">Bu cmdlet 'in Otomasyonu güncelleştirdiği modülün sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="df267-128">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df267-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df267-129">-DefaultProfile</span></span>
<span data-ttu-id="df267-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="df267-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="df267-131">-Ad</span><span class="sxs-lookup"><span data-stu-id="df267-131">-Name</span></span>
<span data-ttu-id="df267-132">Bu cmdlet 'in içeri aktardığından modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df267-132">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="df267-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df267-133">-ResourceGroupName</span></span>
<span data-ttu-id="df267-134">Bu cmdlet 'in modülü güncelleştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="df267-134">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="df267-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df267-135">CommonParameters</span></span>
<span data-ttu-id="df267-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="df267-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df267-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df267-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df267-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="df267-138">INPUTS</span></span>

### <span data-ttu-id="df267-139">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="df267-139">None</span></span>
<span data-ttu-id="df267-140">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="df267-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df267-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="df267-141">OUTPUTS</span></span>

### <span data-ttu-id="df267-142">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="df267-142">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="df267-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="df267-143">NOTES</span></span>

## <span data-ttu-id="df267-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="df267-144">RELATED LINKS</span></span>

[<span data-ttu-id="df267-145">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="df267-145">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="df267-146">Yeni-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="df267-146">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="df267-147">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="df267-147">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)


