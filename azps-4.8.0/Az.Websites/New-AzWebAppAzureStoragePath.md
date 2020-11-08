---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267918"
---
# <span data-ttu-id="8ddc8-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="8ddc8-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="8ddc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ddc8-102">SYNOPSIS</span></span>
<span data-ttu-id="8ddc8-103">Web uygulamasında takılacak bir Azure depolama yolunu temsil eden bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="8ddc8-104">Set-AzWebApp ve Set-AzWebAppSlot için parametre (-AzureStoragePath) olarak kullanılmalıdır.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="8ddc8-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8ddc8-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ddc8-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="8ddc8-106">DESCRIPTION</span></span>
<span data-ttu-id="8ddc8-107">Web uygulamasının içine takılacak bir Azure depolama yolunu temsil eden bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="8ddc8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8ddc8-108">EXAMPLES</span></span>

### <span data-ttu-id="8ddc8-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="8ddc8-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="8ddc8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8ddc8-110">PARAMETERS</span></span>

### <span data-ttu-id="8ddc8-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="8ddc8-111">-AccessKey</span></span>
<span data-ttu-id="8ddc8-112">Azure depolama hesabına erişim anahtarı</span><span class="sxs-lookup"><span data-stu-id="8ddc8-112">Access key to the Azure Storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddc8-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="8ddc8-113">-AccountName</span></span>
<span data-ttu-id="8ddc8-114">Azure depolama hesabı adı.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-114">Azure Storage account name.</span></span>
<span data-ttu-id="8ddc8-115">Örneğin: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="8ddc8-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddc8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ddc8-116">-DefaultProfile</span></span>
<span data-ttu-id="8ddc8-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ddc8-118">-Bağlamayolu</span><span class="sxs-lookup"><span data-stu-id="8ddc8-118">-MountPath</span></span>
<span data-ttu-id="8ddc8-119">Formülde belirtilen paylaşımın sunulacağı kapsayıcıdaki yol</span><span class="sxs-lookup"><span data-stu-id="8ddc8-119">Path in the container where the share specified by ShareName will be exposed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddc8-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="8ddc8-120">-Name</span></span>
<span data-ttu-id="8ddc8-121">Azure depolama özelliğinin tanıtıcısı.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="8ddc8-122">Web uygulaması veya yuvasında benzersiz olmalıdır</span><span class="sxs-lookup"><span data-stu-id="8ddc8-122">Must be unique within the Web App or Slot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddc8-123">-PaylaşımAdı</span><span class="sxs-lookup"><span data-stu-id="8ddc8-123">-ShareName</span></span>
<span data-ttu-id="8ddc8-124">Kapsayıcıya takılacak paylaşımın adı</span><span class="sxs-lookup"><span data-stu-id="8ddc8-124">Name of the share to mount to the container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddc8-125">-Tür</span><span class="sxs-lookup"><span data-stu-id="8ddc8-125">-Type</span></span>
<span data-ttu-id="8ddc8-126">Azure depolama hesabı türü.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="8ddc8-127">Windows kapsayıcıları yalnızca Azure dosyalarını destekler</span><span class="sxs-lookup"><span data-stu-id="8ddc8-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddc8-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="8ddc8-128">-Confirm</span></span>
<span data-ttu-id="8ddc8-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddc8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ddc8-130">-WhatIf</span></span>
<span data-ttu-id="8ddc8-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ddc8-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ddc8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ddc8-133">CommonParameters</span></span>
<span data-ttu-id="8ddc8-134">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8ddc8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ddc8-135">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ddc8-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ddc8-136">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8ddc8-136">INPUTS</span></span>

### <span data-ttu-id="8ddc8-137">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="8ddc8-137">None</span></span>

## <span data-ttu-id="8ddc8-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8ddc8-138">OUTPUTS</span></span>

### <span data-ttu-id="8ddc8-139">Microsoft. Azure. Commands. WebApps. modeller. WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="8ddc8-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="8ddc8-140">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8ddc8-140">NOTES</span></span>

## <span data-ttu-id="8ddc8-141">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8ddc8-141">RELATED LINKS</span></span>
