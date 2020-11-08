---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: d99db4c9fe2c69e2177d9b35e15b49957e910014
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279723"
---
# <span data-ttu-id="7688d-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="7688d-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="7688d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7688d-102">SYNOPSIS</span></span>
<span data-ttu-id="7688d-103">Belirtilen Azure depolama blobundan bir API Yönetim hizmetini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="7688d-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="7688d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7688d-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7688d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7688d-105">DESCRIPTION</span></span>
<span data-ttu-id="7688d-106">**Restore-azın** cmdlet 'i, bir Azurestorage blob içinde belirtilen YEDEKTEN bir API yönetim hizmeti geri yükler.</span><span class="sxs-lookup"><span data-stu-id="7688d-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="7688d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7688d-107">EXAMPLES</span></span>

### <span data-ttu-id="7688d-108">Örnek 1: bir API Yönetim hizmetini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="7688d-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="7688d-109">Bu komut, Azure depolama blob 'dan bir API Yönetim hizmetini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="7688d-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="7688d-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7688d-110">PARAMETERS</span></span>

### <span data-ttu-id="7688d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7688d-111">-DefaultProfile</span></span>
<span data-ttu-id="7688d-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7688d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7688d-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="7688d-113">-Name</span></span>
<span data-ttu-id="7688d-114">Yedeklemeyle birlikte geri yüklenecek API yönetim örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7688d-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7688d-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7688d-115">-PassThru</span></span>
<span data-ttu-id="7688d-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="7688d-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7688d-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="7688d-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7688d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7688d-118">-ResourceGroupName</span></span>
<span data-ttu-id="7688d-119">API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7688d-119">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7688d-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="7688d-120">-SourceBlobName</span></span>
<span data-ttu-id="7688d-121">Azure depolama yedekleme kaynağı blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="7688d-121">Specifies the name of the Azure storage backup source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7688d-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="7688d-122">-SourceContainerName</span></span>
<span data-ttu-id="7688d-123">Azure depolama yedekleme kaynağı kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7688d-123">Specifies the name of the Azure storage backup source container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7688d-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="7688d-124">-StorageContext</span></span>
<span data-ttu-id="7688d-125">Depolama bağlantısı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7688d-125">Specifies the storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7688d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7688d-126">CommonParameters</span></span>
<span data-ttu-id="7688d-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7688d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7688d-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7688d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7688d-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7688d-129">INPUTS</span></span>

### <span data-ttu-id="7688d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7688d-130">System.String</span></span>

## <span data-ttu-id="7688d-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7688d-131">OUTPUTS</span></span>

### <span data-ttu-id="7688d-132">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="7688d-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="7688d-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7688d-133">NOTES</span></span>

## <span data-ttu-id="7688d-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7688d-134">RELATED LINKS</span></span>

[<span data-ttu-id="7688d-135">Yedek-azlı bir</span><span class="sxs-lookup"><span data-stu-id="7688d-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="7688d-136">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="7688d-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="7688d-137">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="7688d-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="7688d-138">Remove-azın</span><span class="sxs-lookup"><span data-stu-id="7688d-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


