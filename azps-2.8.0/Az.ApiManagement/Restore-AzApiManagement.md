---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/restore-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Restore-AzApiManagement.md
ms.openlocfilehash: aa9049489b5a4c28015c208998dae535f514e8f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753439"
---
# <span data-ttu-id="dd41c-101">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="dd41c-101">Restore-AzApiManagement</span></span>

## <span data-ttu-id="dd41c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd41c-102">SYNOPSIS</span></span>
<span data-ttu-id="dd41c-103">Belirtilen Azure depolama blobundan bir API Yönetim hizmetini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="dd41c-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

## <span data-ttu-id="dd41c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dd41c-104">SYNTAX</span></span>

```
Restore-AzApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dd41c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dd41c-105">DESCRIPTION</span></span>
<span data-ttu-id="dd41c-106">**Restore-azın** cmdlet 'i, bir Azurestorage blob içinde belirtilen YEDEKTEN bir API yönetim hizmeti geri yükler.</span><span class="sxs-lookup"><span data-stu-id="dd41c-106">The **Restore-AzApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="dd41c-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dd41c-107">EXAMPLES</span></span>

### <span data-ttu-id="dd41c-108">Örnek 1: bir API Yönetim hizmetini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="dd41c-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Restore-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="dd41c-109">Bu komut, Azure depolama blob 'dan bir API Yönetim hizmetini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="dd41c-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="dd41c-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dd41c-110">PARAMETERS</span></span>

### <span data-ttu-id="dd41c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd41c-111">-DefaultProfile</span></span>
<span data-ttu-id="dd41c-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dd41c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd41c-113">-Ad</span><span class="sxs-lookup"><span data-stu-id="dd41c-113">-Name</span></span>
<span data-ttu-id="dd41c-114">Yedeklemeyle birlikte geri yüklenecek API yönetim örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd41c-114">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="dd41c-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="dd41c-115">-PassThru</span></span>
<span data-ttu-id="dd41c-116">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="dd41c-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="dd41c-117">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="dd41c-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="dd41c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd41c-118">-ResourceGroupName</span></span>
<span data-ttu-id="dd41c-119">API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd41c-119">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="dd41c-120">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="dd41c-120">-SourceBlobName</span></span>
<span data-ttu-id="dd41c-121">Azure depolama yedekleme kaynağı blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd41c-121">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="dd41c-122">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="dd41c-122">-SourceContainerName</span></span>
<span data-ttu-id="dd41c-123">Azure depolama yedekleme kaynağı kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd41c-123">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="dd41c-124">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="dd41c-124">-StorageContext</span></span>
<span data-ttu-id="dd41c-125">Depolama bağlantısı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dd41c-125">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="dd41c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd41c-126">CommonParameters</span></span>
<span data-ttu-id="dd41c-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dd41c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd41c-128">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="dd41c-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd41c-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dd41c-129">INPUTS</span></span>

### <span data-ttu-id="dd41c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dd41c-130">System.String</span></span>

## <span data-ttu-id="dd41c-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dd41c-131">OUTPUTS</span></span>

### <span data-ttu-id="dd41c-132">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="dd41c-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="dd41c-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dd41c-133">NOTES</span></span>

## <span data-ttu-id="dd41c-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dd41c-134">RELATED LINKS</span></span>

[<span data-ttu-id="dd41c-135">Yedek-azlı bir</span><span class="sxs-lookup"><span data-stu-id="dd41c-135">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="dd41c-136">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="dd41c-136">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="dd41c-137">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="dd41c-137">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="dd41c-138">Remove-azın</span><span class="sxs-lookup"><span data-stu-id="dd41c-138">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)


