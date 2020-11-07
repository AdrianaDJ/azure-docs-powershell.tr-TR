---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 022BBF5F-AFF1-45D5-9153-872779FFBAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Restore-AzureRmApiManagement.md
ms.openlocfilehash: 9e19d8e205010ce55886761d2cbb7fd904d5277d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762076"
---
# <span data-ttu-id="219bd-101">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="219bd-101">Restore-AzureRmApiManagement</span></span>

## <span data-ttu-id="219bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="219bd-102">SYNOPSIS</span></span>
<span data-ttu-id="219bd-103">Belirtilen Azure depolama blobundan bir API Yönetim hizmetini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="219bd-103">Restores an API Management Service from the specified Azure storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="219bd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="219bd-104">SYNTAX</span></span>

```
Restore-AzureRmApiManagement -ResourceGroupName <String> -Name <String> [-StorageContext] <IStorageContext>
 -SourceContainerName <String> -SourceBlobName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="219bd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="219bd-105">DESCRIPTION</span></span>
<span data-ttu-id="219bd-106">**Restore-Azurermapsananaks** cmdlet 'i, bir Azurestorage blob 'da bulunan belirtilen YEDEKTEN bir API yönetim hizmeti geri yükler.</span><span class="sxs-lookup"><span data-stu-id="219bd-106">The **Restore-AzureRmApiManagement** cmdlet restores an API Management Service from the specified backup residing in an Azurestorage blob.</span></span>

## <span data-ttu-id="219bd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="219bd-107">EXAMPLES</span></span>

### <span data-ttu-id="219bd-108">Örnek 1: bir API Yönetim hizmetini geri yükleme</span><span class="sxs-lookup"><span data-stu-id="219bd-108">Example 1: Restore an API Management service</span></span>
```
PS C:\>Restore-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "RestoredContosoApi" -StorageContext $StorageContext -SourceContainerName "ContosoBackups" -SourceBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="219bd-109">Bu komut, Azure depolama blob 'dan bir API Yönetim hizmetini geri yükler.</span><span class="sxs-lookup"><span data-stu-id="219bd-109">This command restores an API Management service from Azure storage blob.</span></span>

## <span data-ttu-id="219bd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="219bd-110">PARAMETERS</span></span>

### <span data-ttu-id="219bd-111">-Ad</span><span class="sxs-lookup"><span data-stu-id="219bd-111">-Name</span></span>
<span data-ttu-id="219bd-112">Yedeklemeyle birlikte geri yüklenecek API yönetim örneğinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="219bd-112">Specifies the name of the API Management instance that will be restored with the backup.</span></span>

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

### <span data-ttu-id="219bd-113">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="219bd-113">-PassThru</span></span>
<span data-ttu-id="219bd-114">Çalıştığınız öğeyi temsil eden bir nesne döndürür.</span><span class="sxs-lookup"><span data-stu-id="219bd-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="219bd-115">Varsayılan olarak, bu cmdlet hiçbir çıkış üretmez.</span><span class="sxs-lookup"><span data-stu-id="219bd-115">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="219bd-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219bd-116">-ResourceGroupName</span></span>
<span data-ttu-id="219bd-117">API yönetiminin altında bulunduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="219bd-117">Specifies the name of resource group under which API Management exists.</span></span>

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

### <span data-ttu-id="219bd-118">-SourceBlobName</span><span class="sxs-lookup"><span data-stu-id="219bd-118">-SourceBlobName</span></span>
<span data-ttu-id="219bd-119">Azure depolama yedekleme kaynağı blob 'unu belirtir.</span><span class="sxs-lookup"><span data-stu-id="219bd-119">Specifies the name of the Azure storage backup source blob.</span></span>

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

### <span data-ttu-id="219bd-120">-SourceContainerName</span><span class="sxs-lookup"><span data-stu-id="219bd-120">-SourceContainerName</span></span>
<span data-ttu-id="219bd-121">Azure depolama yedekleme kaynağı kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="219bd-121">Specifies the name of the Azure storage backup source container.</span></span>

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

### <span data-ttu-id="219bd-122">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="219bd-122">-StorageContext</span></span>
<span data-ttu-id="219bd-123">Depolama bağlantısı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="219bd-123">Specifies the storage connection context.</span></span>

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

### <span data-ttu-id="219bd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219bd-124">-DefaultProfile</span></span>
<span data-ttu-id="219bd-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="219bd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="219bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219bd-126">CommonParameters</span></span>
<span data-ttu-id="219bd-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="219bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219bd-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="219bd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219bd-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="219bd-129">INPUTS</span></span>

## <span data-ttu-id="219bd-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="219bd-130">OUTPUTS</span></span>

### <span data-ttu-id="219bd-131">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="219bd-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="219bd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="219bd-132">NOTES</span></span>

## <span data-ttu-id="219bd-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="219bd-133">RELATED LINKS</span></span>

[<span data-ttu-id="219bd-134">Yedek-azurermapı</span><span class="sxs-lookup"><span data-stu-id="219bd-134">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="219bd-135">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="219bd-135">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="219bd-136">Yeni-azurermapı</span><span class="sxs-lookup"><span data-stu-id="219bd-136">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="219bd-137">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="219bd-137">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)


