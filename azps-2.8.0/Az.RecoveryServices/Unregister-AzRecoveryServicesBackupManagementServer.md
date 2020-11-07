---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupmanagementserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 5452758a5cf269ef50475b8962e5fbca117dbb1d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933430"
---
# <span data-ttu-id="19841-101">Unregister-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="19841-101">Unregister-AzRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="19841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19841-102">SYNOPSIS</span></span>
<span data-ttu-id="19841-103">Bir SCDPM sunucusunun veya yedek sunucunun kasasından kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="19841-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

## <span data-ttu-id="19841-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="19841-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19841-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="19841-105">DESCRIPTION</span></span>
<span data-ttu-id="19841-106">**Unregister-AzRecoveryServicesBackupManagementServer** cmdlet 'ı bir System Center Data Protection Manager (SCDPM) sunucusunun veya kasadan bir Azure yedekleme sunucusunun kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="19841-106">The **Unregister-AzRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="19841-107">Bu cmdlet, kasadaki kaydedilmemiş sunuculara yapılan başvuruları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="19841-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>
<span data-ttu-id="19841-108">Bir kapsayıcının kaydını silebilmek için, bu kapsayıcıyla ilişkili tüm korumalı verileri silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="19841-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="19841-109">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="19841-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="19841-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="19841-110">EXAMPLES</span></span>

### <span data-ttu-id="19841-111">Örnek 1: kasadan SCDPM sunucusunun kaydını silme</span><span class="sxs-lookup"><span data-stu-id="19841-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupManagementServer -AzBackupManagementServer $BMS
```

<span data-ttu-id="19841-112">İlk komut dpmserver01.contoso.com adındaki yedekleme yönetim sunucusunu alır ve $BMS değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="19841-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>
<span data-ttu-id="19841-113">İkinci komut, listeden SCDPM sunucusunu siler.</span><span class="sxs-lookup"><span data-stu-id="19841-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="19841-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="19841-114">PARAMETERS</span></span>

### <span data-ttu-id="19841-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="19841-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="19841-116">Kurtarma Hizmetleri yedek kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="19841-116">The recovery services backup container.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19841-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19841-117">-DefaultProfile</span></span>
<span data-ttu-id="19841-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="19841-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19841-119">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="19841-119">-PassThru</span></span>
<span data-ttu-id="19841-120">Silinecek yedekleme yönetim sunucusunu döndür.</span><span class="sxs-lookup"><span data-stu-id="19841-120">Return the Backup Management Server to be deleted.</span></span>

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

### <span data-ttu-id="19841-121">-VaultId</span><span class="sxs-lookup"><span data-stu-id="19841-121">-VaultId</span></span>
<span data-ttu-id="19841-122">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="19841-122">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19841-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="19841-123">-Confirm</span></span>
<span data-ttu-id="19841-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="19841-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19841-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19841-125">-WhatIf</span></span>
<span data-ttu-id="19841-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="19841-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19841-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="19841-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19841-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19841-128">CommonParameters</span></span>
<span data-ttu-id="19841-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="19841-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19841-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19841-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19841-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="19841-131">INPUTS</span></span>

### <span data-ttu-id="19841-132">System. String</span><span class="sxs-lookup"><span data-stu-id="19841-132">System.String</span></span>

## <span data-ttu-id="19841-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="19841-133">OUTPUTS</span></span>

### <span data-ttu-id="19841-134">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. BackupEngineBase</span><span class="sxs-lookup"><span data-stu-id="19841-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupEngineBase</span></span>

## <span data-ttu-id="19841-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="19841-135">NOTES</span></span>

## <span data-ttu-id="19841-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="19841-136">RELATED LINKS</span></span>

[<span data-ttu-id="19841-137">Get-AzRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="19841-137">Get-AzRecoveryServicesBackupManagementServer</span></span>](./Get-AzRecoveryServicesBackupManagementServer.md)


