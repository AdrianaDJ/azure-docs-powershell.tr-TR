---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106223"
---
# <span data-ttu-id="6ab06-101">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6ab06-101">New-AzureAutomationModule</span></span>

## <span data-ttu-id="6ab06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ab06-102">SYNOPSIS</span></span>

<span data-ttu-id="6ab06-103">Bir modülü otomatikleştirme 'ye aktarır.</span><span class="sxs-lookup"><span data-stu-id="6ab06-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="6ab06-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ab06-104">SYNTAX</span></span>

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="6ab06-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ab06-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="6ab06-106">**New-AzureAutomationModule** cmdlet 'ı Azure Otomasyonu 'nda modül içeri aktarır.</span><span class="sxs-lookup"><span data-stu-id="6ab06-106">The **New-AzureAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="6ab06-107">Modül, aşağıdaki dosya türlerinden birini içeren bir klasör içeren,. zip uzantılı sıkıştırılmış bir dosyadır:</span><span class="sxs-lookup"><span data-stu-id="6ab06-107">A module is a compressed file, with a .zip extension, that contains a folder which includes one of the following file types:</span></span>

- <span data-ttu-id="6ab06-108">Windows PowerShell modülü (psm1 dosyası).</span><span class="sxs-lookup"><span data-stu-id="6ab06-108">A Windows PowerShell module (psm1 file).</span></span> 

- <span data-ttu-id="6ab06-109">Windows PowerShell modülü bildirimi (psd1 dosyası).</span><span class="sxs-lookup"><span data-stu-id="6ab06-109">A Windows PowerShell module manifest (psd1 file).</span></span> 

- <span data-ttu-id="6ab06-110">Derleme (dll dosyası).</span><span class="sxs-lookup"><span data-stu-id="6ab06-110">An assembly (dll file).</span></span>

<span data-ttu-id="6ab06-111">Zip dosyasının adları, ZIP dosyasındaki klasör ve klasördeki (. psm1, PSD. 1 veya. dll) dosya eşleşmelidir.</span><span class="sxs-lookup"><span data-stu-id="6ab06-111">The names of the zip file, the folder in the zip file, and file in the folder (.psm1, psd.1, or .dll) must match.</span></span>

## <span data-ttu-id="6ab06-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ab06-112">EXAMPLES</span></span>

### <span data-ttu-id="6ab06-113">Örnek 1: modül Içeri aktarma</span><span class="sxs-lookup"><span data-stu-id="6ab06-113">Example 1: Import a module</span></span>
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

<span data-ttu-id="6ab06-114">Bu komut, ContosoModule adlı bir modülü Contoso17 adlı Otomasyon hesabına aktarır.</span><span class="sxs-lookup"><span data-stu-id="6ab06-114">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="6ab06-115">Modül, bir Azure Blob 'unda, contosostorage adlı bir depolama hesabında ve modüller adlı bir kapsayıcı içinde depolanır.</span><span class="sxs-lookup"><span data-stu-id="6ab06-115">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="6ab06-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ab06-116">PARAMETERS</span></span>

### <span data-ttu-id="6ab06-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6ab06-117">-AutomationAccountName</span></span>
<span data-ttu-id="6ab06-118">Modülün saklanacağı Otomasyon hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ab06-118">Specifies the name of the Automation account the module will be stored in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab06-119">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="6ab06-119">-ContentLink</span></span>
<span data-ttu-id="6ab06-120">Web sitesi veya modül dosyasının yolunu belirten Azure Blob deposu gibi ortak URL.</span><span class="sxs-lookup"><span data-stu-id="6ab06-120">Public URL such as a website or Azure blob storage specifying the path to the module file.</span></span>
<span data-ttu-id="6ab06-121">Bu konuma publicolarak erişilebilir olması gerekir.</span><span class="sxs-lookup"><span data-stu-id="6ab06-121">This location must be publically accessible.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab06-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="6ab06-122">-Name</span></span>
<span data-ttu-id="6ab06-123">Modül için bir ad belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ab06-123">Specifies a name for the module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab06-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="6ab06-124">-Profile</span></span>
<span data-ttu-id="6ab06-125">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ab06-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="6ab06-126">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="6ab06-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ab06-127">-Etiketler</span><span class="sxs-lookup"><span data-stu-id="6ab06-127">-Tags</span></span>
<span data-ttu-id="6ab06-128">Modülle ilgili bir veya daha fazla etiketi belirtir.</span><span class="sxs-lookup"><span data-stu-id="6ab06-128">Specifies one or more tags related to the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ab06-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ab06-129">CommonParameters</span></span>
<span data-ttu-id="6ab06-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ab06-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ab06-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ab06-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ab06-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ab06-132">INPUTS</span></span>

## <span data-ttu-id="6ab06-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ab06-133">OUTPUTS</span></span>

### <span data-ttu-id="6ab06-134">Microsoft. Azure. Commands. Automation. model. Module</span><span class="sxs-lookup"><span data-stu-id="6ab06-134">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="6ab06-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ab06-135">NOTES</span></span>

## <span data-ttu-id="6ab06-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ab06-136">RELATED LINKS</span></span>

[<span data-ttu-id="6ab06-137">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6ab06-137">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="6ab06-138">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6ab06-138">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="6ab06-139">Set-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6ab06-139">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


