---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5846BBB7-DA8E-41B5-A894-BA2B61C2212C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/backup-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Backup-AzApiManagement.md
ms.openlocfilehash: 576c623b942ec496d2800c1ad5432f72eb6911bc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93751183"
---
# <span data-ttu-id="0d884-101">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="0d884-101">Backup-AzApiManagement</span></span>

## <span data-ttu-id="0d884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d884-102">SYNOPSIS</span></span>
<span data-ttu-id="0d884-103">Bir API Yönetim hizmetini yedekler.</span><span class="sxs-lookup"><span data-stu-id="0d884-103">Backs up an API Management service.</span></span>

## <span data-ttu-id="0d884-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0d884-104">SYNTAX</span></span>

```
Backup-AzApiManagement -ResourceGroupName <String> -Name <String> -StorageContext <IStorageContext>
 -TargetContainerName <String> [-TargetBlobName <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d884-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0d884-105">DESCRIPTION</span></span>
<span data-ttu-id="0d884-106">**Backup-azın** cmdlet 'ı BIR Azure API yönetim hizmeti örneğini yedekler.</span><span class="sxs-lookup"><span data-stu-id="0d884-106">The **Backup-AzApiManagement** cmdlet backs up an instance of an Azure API Management service.</span></span>
<span data-ttu-id="0d884-107">Bu cmdlet yedeği bir Azure Depolama Blobu olarak depolar.</span><span class="sxs-lookup"><span data-stu-id="0d884-107">This cmdlet stores the backup as an Azure Storage blob.</span></span>

## <span data-ttu-id="0d884-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0d884-108">EXAMPLES</span></span>

### <span data-ttu-id="0d884-109">Örnek 1: bir API Yönetim hizmetini yedekleme</span><span class="sxs-lookup"><span data-stu-id="0d884-109">Example 1: Back up an API Management service</span></span>
```
PS C:\>New-AzStorageAccount -StorageAccountName "ContosoStorage" -Location $location -ResourceGroupName "ContosoGroup02" -Type Standard_LRS
PS C:\>$storageKey = (Get-AzStorageAccountKey -ResourceGroupName "ContosoGroup02" -StorageAccountName "ContosoStorage")[0].Value
PS C:\>$storageContext = New-AzStorageContext -StorageAccountName "ContosoStorage" -StorageAccountKey $storageKey
PS C:\>Backup-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -StorageContext $StorageContext -TargetContainerName "ContosoBackups" -TargetBlobName "ContosoBackup.apimbackup"
```

<span data-ttu-id="0d884-110">Bu komut, bir API Yönetim hizmetini bir depolama blob 'una yedekler.</span><span class="sxs-lookup"><span data-stu-id="0d884-110">This command backs up an API Management service to a Storage blob.</span></span>

## <span data-ttu-id="0d884-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0d884-111">PARAMETERS</span></span>

### <span data-ttu-id="0d884-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d884-112">-DefaultProfile</span></span>
<span data-ttu-id="0d884-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0d884-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d884-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="0d884-114">-Name</span></span>
<span data-ttu-id="0d884-115">Bu cmdlet 'in yedeklediği API yönetim dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d884-115">Specifies the name of the API Management deployment that this cmdlet backs up.</span></span>

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

### <span data-ttu-id="0d884-116">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0d884-116">-PassThru</span></span>
<span data-ttu-id="0d884-117">İşlem başarılı olursa, bu cmdlet 'in yedeklenen **Psapımana,** nesnesini döndürmediğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d884-117">Indicates that this cmdlet returns the backed up **PsApiManagement** object, if the operation succeeds.</span></span>

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

### <span data-ttu-id="0d884-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d884-118">-ResourceGroupName</span></span>
<span data-ttu-id="0d884-119">API yönetim dağıtımının olduğu kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d884-119">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="0d884-120">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="0d884-120">-StorageContext</span></span>
<span data-ttu-id="0d884-121">Bir depolama bağlantı bağlamını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d884-121">Specifies a storage connection context.</span></span>

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

### <span data-ttu-id="0d884-122">-TargetBlobName</span><span class="sxs-lookup"><span data-stu-id="0d884-122">-TargetBlobName</span></span>
<span data-ttu-id="0d884-123">Yedeklemenin blob adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d884-123">Specifies the name of the blob for the backup.</span></span>
<span data-ttu-id="0d884-124">Blob yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0d884-124">If the blob does not exist, this cmdlet creates it.</span></span>
<span data-ttu-id="0d884-125">Bu cmdlet, aşağıdaki desene dayalı olarak varsayılan bir değer oluşturur: {Name}-{yyyy-aa-dd-ss-dd}. apsanbackup</span><span class="sxs-lookup"><span data-stu-id="0d884-125">This cmdlet generates a default value based on the following pattern: {Name}-{yyyy-MM-dd-HH-mm}.apimbackup</span></span>

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

### <span data-ttu-id="0d884-126">-TargetContainerName</span><span class="sxs-lookup"><span data-stu-id="0d884-126">-TargetContainerName</span></span>
<span data-ttu-id="0d884-127">Yedeklemenin blob kapsayıcısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0d884-127">Specifies the name of the container of the blob for the backup.</span></span>
<span data-ttu-id="0d884-128">Konteyner yoksa, bu cmdlet bunu oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0d884-128">If the container does not exist, this cmdlet creates it.</span></span>

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

### <span data-ttu-id="0d884-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d884-129">CommonParameters</span></span>
<span data-ttu-id="0d884-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0d884-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d884-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d884-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d884-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0d884-132">INPUTS</span></span>

### <span data-ttu-id="0d884-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0d884-133">System.String</span></span>

### <span data-ttu-id="0d884-134">Microsoft. Azure. Commands. Common. Authentication. soyutlamalar. ıstoragecontext</span><span class="sxs-lookup"><span data-stu-id="0d884-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0d884-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0d884-135">OUTPUTS</span></span>

### <span data-ttu-id="0d884-136">Microsoft. Azure. Commands. apsanana</span><span class="sxs-lookup"><span data-stu-id="0d884-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0d884-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0d884-137">NOTES</span></span>

## <span data-ttu-id="0d884-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0d884-138">RELATED LINKS</span></span>

[<span data-ttu-id="0d884-139">Get-Azıbir</span><span class="sxs-lookup"><span data-stu-id="0d884-139">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="0d884-140">Yeni-azlı bir</span><span class="sxs-lookup"><span data-stu-id="0d884-140">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="0d884-141">Remove-azın</span><span class="sxs-lookup"><span data-stu-id="0d884-141">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="0d884-142">Geri yükleme-azbir</span><span class="sxs-lookup"><span data-stu-id="0d884-142">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)

