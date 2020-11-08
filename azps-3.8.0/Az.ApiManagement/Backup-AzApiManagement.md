---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: fcdd498c99c10857e0fa76c890bc6be6e9733b84
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097440"
---
# <span data-ttu-id="4385f-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4385f-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="4385f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4385f-102">SYNOPSIS</span></span>
<span data-ttu-id="4385f-103">Bir API Yönetim hizmetini yedekler.</span><span class="sxs-lookup"><span data-stu-id="4385f-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="4385f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4385f-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4385f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="4385f-105">DESCRIPTION</span></span>
<span data-ttu-id="4385f-106">**Backup-azın** cmdlet 'ı BIR Azure API yönetim hizmeti örneğini yedekler.</span><span class="sxs-lookup"><span data-stu-id="4385f-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="4385f-107">Bu cmdlet yedeği bir Azure Depolama Blobu olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="4385f-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="4385f-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4385f-108">EXAMPLES</span></span>

### <span data-ttu-id="4385f-109">Örnek 1: bir API Yönetim hizmetini yedekleme</span><span class="sxs-lookup"><span data-stu-id="4385f-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="4385f-110">Bu komut, bir API Yönetim hizmetini bir depolama blob 'una yedekler.</span><span class="sxs-lookup"><span data-stu-id="4385f-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="4385f-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4385f-111">PARAMETERS</span></span>

### <span data-ttu-id="4385f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4385f-112">-DefaultProfile</span></span>
<span data-ttu-id="4385f-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4385f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4385f-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="4385f-114">-Name</span></span>
<span data-ttu-id="4385f-115">Bu cmdlet 'in yedeklediği API yönetim dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4385f-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="4385f-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="4385f-116">-PassThru</span></span>
<span data-ttu-id="4385f-117">İşlem başarılı olursa, bu cmdlet 'in yedeklenen **Psapımana,** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="4385f-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="4385f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4385f-118">-ResourceGroupName</span></span>
<span data-ttu-id="4385f-119">API yönetim dağıtımının olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4385f-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="4385f-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="4385f-120">-StorageContext</span></span>
<span data-ttu-id="4385f-121">Bir depolama bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4385f-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="4385f-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="4385f-122">-TargetBlobName</span></span>
<span data-ttu-id="4385f-123">Yedeklemenin blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4385f-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="4385f-124">Blob yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4385f-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="4385f-125">Bu cmdlet, aşağıdaki desene dayalı olarak varsayılan bir değer oluşturur: {Name}-{yyyy-aa-dd-ss-dd}. apsanbackup</span><span class="sxs-lookup"><span data-stu-id="4385f-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="4385f-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="4385f-126">-TargetContainerName</span></span>
<span data-ttu-id="4385f-127">Yedeklemenin blob kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="4385f-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="4385f-128">Konteyner yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="4385f-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="4385f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4385f-129">CommonParameters</span></span>
<span data-ttu-id="4385f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4385f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4385f-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="4385f-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4385f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4385f-132">INPUTS</span></span>

### <span data-ttu-id="4385f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4385f-133">System.String</span></span>

### <span data-ttu-id="4385f-134">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="4385f-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4385f-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4385f-135">OUTPUTS</span></span>

### <span data-ttu-id="4385f-136">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="4385f-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="4385f-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4385f-137">NOTES</span></span>

## <span data-ttu-id="4385f-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4385f-138">RELATED LINKS</span></span>

[<span data-ttu-id="4385f-139">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="4385f-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="4385f-140">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="4385f-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="4385f-141">Remove-azın</span><span class="sxs-lookup"><span data-stu-id="4385f-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="4385f-142">Geri yükleme-azbir</span><span class="sxs-lookup"><span data-stu-id="4385f-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)

