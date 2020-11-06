---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/backup-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Backup-AzureRmApiManagement.md
ms.openlocfilehash: d8f243b0b02d724a3979b8c8f318be8e58623cf5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592829"
---
# <span data-ttu-id="2d58a-101">Backup-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d58a-101">Backup-AzureRmApiManagement</span></span>

## <span data-ttu-id="2d58a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d58a-102">SYNOPSIS</span></span>
<span data-ttu-id="2d58a-103">Bir API Yönetim hizmetini yedekler.</span><span class="sxs-lookup"><span data-stu-id="2d58a-103">Backs up an API Management service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d58a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2d58a-104">SYNTAX</span></span>

```
Backup-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d58a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="2d58a-105">DESCRIPTION</span></span>
<span data-ttu-id="2d58a-106">**Backup-Azurermapsananaes** cmdlet 'ı BIR Azure API yönetim hizmeti örneğini yedekler.</span><span class="sxs-lookup"><span data-stu-id="2d58a-106">The **Backup-AzureRmApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="2d58a-107">Bu cmdlet yedeği bir Azure Depolama Blobu olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="2d58a-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="2d58a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2d58a-108">EXAMPLES</span></span>

### <span data-ttu-id="2d58a-109">Örnek 1: bir API Yönetim hizmetini yedekleme</span><span class="sxs-lookup"><span data-stu-id="2d58a-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzureRmStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzureRmStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzureStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="2d58a-110">Bu komut, bir API Yönetim hizmetini bir depolama blob 'una yedekler.</span><span class="sxs-lookup"><span data-stu-id="2d58a-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="2d58a-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2d58a-111">PARAMETERS</span></span>

### <span data-ttu-id="2d58a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d58a-112">-DefaultProfile</span></span>
<span data-ttu-id="2d58a-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2d58a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d58a-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="2d58a-114">-Name</span></span>
<span data-ttu-id="2d58a-115">Bu cmdlet 'in yedeklediği API yönetim dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d58a-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="2d58a-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="2d58a-116">-PassThru</span></span>
<span data-ttu-id="2d58a-117">İşlem başarılı olursa, bu cmdlet 'in yedeklenen **Psapımana,** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d58a-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="2d58a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d58a-118">-ResourceGroupName</span></span>
<span data-ttu-id="2d58a-119">API yönetim dağıtımının olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d58a-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="2d58a-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="2d58a-120">-StorageContext</span></span>
<span data-ttu-id="2d58a-121">Bir depolama bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d58a-121">Specifies a storage connection context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d58a-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="2d58a-122">-TargetBlobName</span></span>
<span data-ttu-id="2d58a-123">Yedeklemenin blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d58a-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="2d58a-124">Blob yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d58a-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="2d58a-125">Bu cmdlet, aşağıdaki desene dayalı olarak varsayılan bir değer oluşturur: {Name}-{yyyy-aa-dd-ss-dd}. apsanbackup</span><span class="sxs-lookup"><span data-stu-id="2d58a-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d58a-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="2d58a-126">-TargetContainerName</span></span>
<span data-ttu-id="2d58a-127">Yedeklemenin blob kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="2d58a-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="2d58a-128">Konteyner yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="2d58a-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="2d58a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d58a-129">CommonParameters</span></span>
<span data-ttu-id="2d58a-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2d58a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d58a-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d58a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d58a-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2d58a-132">INPUTS</span></span>

### <span data-ttu-id="2d58a-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2d58a-133">System.String</span></span>

### <span data-ttu-id="2d58a-134">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="2d58a-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2d58a-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2d58a-135">OUTPUTS</span></span>

### <span data-ttu-id="2d58a-136">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="2d58a-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2d58a-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2d58a-137">NOTES</span></span>

## <span data-ttu-id="2d58a-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2d58a-138">RELATED LINKS</span></span>

[<span data-ttu-id="2d58a-139">Get-azurermapı</span><span class="sxs-lookup"><span data-stu-id="2d58a-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="2d58a-140">Yeni-azurermapı</span><span class="sxs-lookup"><span data-stu-id="2d58a-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="2d58a-141">Remove-azurermapsanana</span><span class="sxs-lookup"><span data-stu-id="2d58a-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="2d58a-142">Geri yükleme-azurermapı</span><span class="sxs-lookup"><span data-stu-id="2d58a-142">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


