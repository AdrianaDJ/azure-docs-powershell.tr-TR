---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937398"
---
# <span data-ttu-id="c8a03-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c8a03-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="c8a03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8a03-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a03-103">Otomasyon 'da bir modülü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c8a03-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="c8a03-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c8a03-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c8a03-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c8a03-105">DESCRIPTION</span></span>
<span data-ttu-id="c8a03-106">**Set-AzAutomationModule** cmdlet 'ı Azure Otomasyonu 'nda bir modülü güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="c8a03-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="c8a03-107">Bu komut,. zip dosya adı uzantısına sahip sıkıştırılmış bir dosyayı kabul eder.</span><span class="sxs-lookup"><span data-stu-id="c8a03-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="c8a03-108">Dosya, aşağıdaki türlerden birine sahip bir dosya içeren bir klasör içerir:</span><span class="sxs-lookup"><span data-stu-id="c8a03-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="c8a03-109">. psm1 veya. dll dosya adı uzantısına sahip wps_2 modülü</span><span class="sxs-lookup"><span data-stu-id="c8a03-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="c8a03-110">. psd1 dosya adı uzantısına sahip wps_2 modül bildirimi,. zip dosyasının adı, klasörün adı ve klasörün adı aynı olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c8a03-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="c8a03-111">. Zip dosyasını Otomasyon hizmetinin erişebileceği bir URL olarak belirtin.</span><span class="sxs-lookup"><span data-stu-id="c8a03-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="c8a03-112">Bu cmdlet veya New-AzAutomationModule cmdlet 'ini kullanarak bir wps_2 modülünü Otomasyonu</span><span class="sxs-lookup"><span data-stu-id="c8a03-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="c8a03-113">Bu komut almanın başarılı veya başarısız olduğunu sonlandırır.</span><span class="sxs-lookup"><span data-stu-id="c8a03-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="c8a03-114">Başarılı olup olmadığını denetlemek için, aşağıdaki komutu çalıştırarak: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` ModuleName başarılı bir şekilde **provisioningstate** özelliğini denetleyin.</span><span class="sxs-lookup"><span data-stu-id="c8a03-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="c8a03-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c8a03-115">EXAMPLES</span></span>

### <span data-ttu-id="c8a03-116">Örnek 1: modül güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="c8a03-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c8a03-117">Bu komut, Contoso17 adlı Otomasyon hesabına ContosoModule adlı var olan bir modülün güncelleştirilmiş sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="c8a03-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="c8a03-118">Modül, bir Azure Blob 'unda, contosostorage adlı bir depolama hesabında ve modüller adlı bir kapsayıcı içinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="c8a03-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="c8a03-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c8a03-119">PARAMETERS</span></span>

### <span data-ttu-id="c8a03-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c8a03-120">-AutomationAccountName</span></span>
<span data-ttu-id="c8a03-121">Bu cmdlet 'in modülü güncelleştirdiği Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8a03-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="c8a03-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="c8a03-122">-ContentLinkUri</span></span>
<span data-ttu-id="c8a03-123">Bu cmdlet 'in içeri aktardığından, modülün yeni sürümünü içeren. zip dosyasının URL 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8a03-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="c8a03-124">-ContentLinkVersion</span></span>
<span data-ttu-id="c8a03-125">Bu cmdlet 'in Otomasyonu güncelleştirdiği modülün sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8a03-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c8a03-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a03-126">-DefaultProfile</span></span>
<span data-ttu-id="c8a03-127">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c8a03-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c8a03-128">-Ad</span><span class="sxs-lookup"><span data-stu-id="c8a03-128">-Name</span></span>
<span data-ttu-id="c8a03-129">Bu cmdlet 'in içeri aktardığından modülün adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8a03-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="c8a03-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a03-130">-ResourceGroupName</span></span>
<span data-ttu-id="c8a03-131">Bu cmdlet 'in modülü güncelleştirdiği kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="c8a03-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="c8a03-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a03-132">CommonParameters</span></span>
<span data-ttu-id="c8a03-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c8a03-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a03-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8a03-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a03-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c8a03-135">INPUTS</span></span>

### <span data-ttu-id="c8a03-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c8a03-136">System.String</span></span>

### <span data-ttu-id="c8a03-137">System. Uri</span><span class="sxs-lookup"><span data-stu-id="c8a03-137">System.Uri</span></span>

## <span data-ttu-id="c8a03-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c8a03-138">OUTPUTS</span></span>

### <span data-ttu-id="c8a03-139">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="c8a03-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="c8a03-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c8a03-140">NOTES</span></span>

## <span data-ttu-id="c8a03-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c8a03-141">RELATED LINKS</span></span>

[<span data-ttu-id="c8a03-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c8a03-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="c8a03-143">Yeni-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c8a03-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="c8a03-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c8a03-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

