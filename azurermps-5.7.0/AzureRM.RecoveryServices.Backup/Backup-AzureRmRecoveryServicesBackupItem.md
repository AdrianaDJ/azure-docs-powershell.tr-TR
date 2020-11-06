---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/backup-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Backup-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a7451855f62a9e0eab63936107d8431342badfb4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593455"
---
# <span data-ttu-id="ab7b9-101">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="ab7b9-101">Backup-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="ab7b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ab7b9-103">Yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-103">Starts a backup for a Backup item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab7b9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ab7b9-104">SYNTAX</span></span>

```
Backup-AzureRmRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab7b9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ab7b9-105">DESCRIPTION</span></span>
<span data-ttu-id="ab7b9-106">**Backup-Azurermrecoveryservicesbackupıtem** cmdlet 'i, yedekleme zamanlamasına bağlı olmayan korumalı bir Azure yedekleme öğesi için yedekleme başlatır.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-106">The **Backup-AzureRmRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="ab7b9-107">Zamanlanmış bir yedekleme başarısız olduktan sonra, korumayı etkinleştirdikten veya yedekleme başlattıktan sonra bir ilk yedekleme yapabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>

<span data-ttu-id="ab7b9-108">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-108">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ab7b9-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ab7b9-109">EXAMPLES</span></span>

### <span data-ttu-id="ab7b9-110">Örnek 1: yedekleme öğesi için yedekleme başlatma</span><span class="sxs-lookup"><span data-stu-id="ab7b9-110">Example 1: Start a backup for a Backup item</span></span>
```
PS C:\> $NamedContainer = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "pstestv2vm1" 
PS C:\> $Item = Get-AzureRmRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM 
PS C:\> $Job = Backup-AzureRmRecoveryServicesItem -Item $Item
Operation        Status               StartTime            EndTime                   JOBID                           
------------     ---------            ------               ---------                 -------                                         
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="ab7b9-111">İlk komut, AzureVM türünün pstestv2vm1 adındaki yedekleme kapsayıcısını alır ve $NamedContainer değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>

<span data-ttu-id="ab7b9-112">İkinci komut $NamedContainer kapsayıcısına karşılık gelen yedekleme öğesini alır ve $Item değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>

<span data-ttu-id="ab7b9-113">Son komut $Item içindeki yedekleme öğesi için yedekleme işini tetikler.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="ab7b9-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ab7b9-114">PARAMETERS</span></span>

### <span data-ttu-id="ab7b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab7b9-115">-DefaultProfile</span></span>
<span data-ttu-id="ab7b9-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab7b9-117">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="ab7b9-117">-ExpiryDateTimeUTC</span></span>
<span data-ttu-id="ab7b9-118">**Tarih saat** nesnesi olarak sona erme zamanını belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-118">Specifies an expiry time as a **DateTime** object.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7b9-119">-Öğe</span><span class="sxs-lookup"><span data-stu-id="ab7b9-119">-Item</span></span>
<span data-ttu-id="ab7b9-120">Bu cmdlet 'in yedekleme işlemini başlattığı yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-120">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: ItemBase
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab7b9-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="ab7b9-121">-Confirm</span></span>
<span data-ttu-id="ab7b9-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7b9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab7b9-123">-WhatIf</span></span>
<span data-ttu-id="ab7b9-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab7b9-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab7b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab7b9-126">CommonParameters</span></span>
<span data-ttu-id="ab7b9-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ab7b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab7b9-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab7b9-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab7b9-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ab7b9-129">INPUTS</span></span>

### <span data-ttu-id="ab7b9-130">Saniy</span><span class="sxs-lookup"><span data-stu-id="ab7b9-130">DateTime</span></span>
<span data-ttu-id="ab7b9-131">' ExpiryDateTimeUTC ' parametresi ardışık düzenin ' TarihSaat ' türünün değerini kabul eder</span><span class="sxs-lookup"><span data-stu-id="ab7b9-131">Parameter 'ExpiryDateTimeUTC' accepts value of type 'DateTime' from the pipeline</span></span>

### <span data-ttu-id="ab7b9-132">Itembase</span><span class="sxs-lookup"><span data-stu-id="ab7b9-132">ItemBase</span></span>
<span data-ttu-id="ab7b9-133">Parametre ' öğe ', ardışık düzen</span><span class="sxs-lookup"><span data-stu-id="ab7b9-133">Parameter 'Item' accepts value of type 'ItemBase' from the pipeline</span></span>

## <span data-ttu-id="ab7b9-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ab7b9-134">OUTPUTS</span></span>

### <span data-ttu-id="ab7b9-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. JobBase</span><span class="sxs-lookup"><span data-stu-id="ab7b9-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ab7b9-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ab7b9-136">NOTES</span></span>

## <span data-ttu-id="ab7b9-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ab7b9-137">RELATED LINKS</span></span>

[<span data-ttu-id="ab7b9-138">Get-AzureRmRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="ab7b9-138">Get-AzureRmRecoveryServicesBackupContainer</span></span>](./Get-AzureRmRecoveryServicesBackupContainer.md)

[<span data-ttu-id="ab7b9-139">Get-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ab7b9-139">Get-AzureRmRecoveryServicesBackupItem</span></span>](./Get-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="ab7b9-140">Restore-Azurermrecoveryservicesbackupıtem</span><span class="sxs-lookup"><span data-stu-id="ab7b9-140">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


