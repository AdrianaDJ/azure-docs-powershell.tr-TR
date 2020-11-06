---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: BBF12B16-C5FD-4AE2-B5D7-AFDC29CEE4D3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Unregister-AzureRmRecoveryServicesBackupManagementServer.md
ms.openlocfilehash: 1b025825878e2bc97837237e194b0ec37eb298d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593045"
---
# <span data-ttu-id="b7910-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="b7910-101">Unregister-AzureRmRecoveryServicesBackupManagementServer</span></span>

## <span data-ttu-id="b7910-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7910-102">SYNOPSIS</span></span>
<span data-ttu-id="b7910-103">Bir SCDPM sunucusunun veya yedek sunucunun kasasından kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="b7910-103">Unregisters a SCDPM server or Backup server from the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7910-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b7910-104">SYNTAX</span></span>

```
Unregister-AzureRmRecoveryServicesBackupManagementServer [-AzureRmBackupManagementServer] <BackupEngineBase>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7910-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b7910-105">DESCRIPTION</span></span>
<span data-ttu-id="b7910-106">**Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet 'ı bir System Center Data Protection Manager (SCDPM) sunucusunun veya kasadan bir Azure yedekleme sunucusunun kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="b7910-106">The **Unregister-AzureRmRecoveryServicesBackupManagementServer** cmdlet unregisters a System Center Data Protection Manager (SCDPM) server or an Azure Backup server from the vault.</span></span>
<span data-ttu-id="b7910-107">Bu cmdlet, kasadaki kaydedilmemiş sunuculara yapılan başvuruları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="b7910-107">This cmdlet removes references to the servers that are unregistered from the vault.</span></span>

<span data-ttu-id="b7910-108">Bir kapsayıcının kaydını silebilmek için, bu kapsayıcıyla ilişkili tüm korumalı verileri silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b7910-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>

<span data-ttu-id="b7910-109">Geçerli cmdlet 'i kullanmadan önce Set-AzureRmRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="b7910-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b7910-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b7910-110">EXAMPLES</span></span>

### <span data-ttu-id="b7910-111">Örnek 1: kasadan SCDPM sunucusunun kaydını silme</span><span class="sxs-lookup"><span data-stu-id="b7910-111">Example 1: Unregister an SCDPM server from the vault</span></span>
```
PS C:\>$BMS = Get-AzureRmRecoveryServicesBackupManagementServer -Name "dpmserver01.contoso.com"
PS C:\> Unregister-AzureRmRecoveryServicesBackupManagementServer -AzureRmBackupManagementServer $BMS
```

<span data-ttu-id="b7910-112">İlk komut dpmserver01.contoso.com adındaki yedekleme yönetim sunucusunu alır ve $BMS değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="b7910-112">The first command gets the Backup management server named dpmserver01.contoso.com, and then stores it in the $BMS variable.</span></span>

<span data-ttu-id="b7910-113">İkinci komut, listeden SCDPM sunucusunu siler.</span><span class="sxs-lookup"><span data-stu-id="b7910-113">The second command unregisters the SCDPM server from the vault.</span></span>

## <span data-ttu-id="b7910-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b7910-114">PARAMETERS</span></span>

### <span data-ttu-id="b7910-115">-AzureRmBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="b7910-115">-AzureRmBackupManagementServer</span></span>
<span data-ttu-id="b7910-116">Kaydı kaldırmak için bir SCDPM sunucu nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="b7910-116">Specifies an SCDPM server object to unregister.</span></span>
<span data-ttu-id="b7910-117">**Backupmanagementserver** nesnesi edinmek için Get-AzureRmRecoveryServicesBackupManagementServer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="b7910-117">To obtain an **BackupManagementServer** object, use the Get-AzureRmRecoveryServicesBackupManagementServer cmdlet.</span></span>

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

### <span data-ttu-id="b7910-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7910-118">-DefaultProfile</span></span>
<span data-ttu-id="b7910-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b7910-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b7910-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7910-120">CommonParameters</span></span>
<span data-ttu-id="b7910-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b7910-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7910-122">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7910-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7910-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b7910-123">INPUTS</span></span>

## <span data-ttu-id="b7910-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b7910-124">OUTPUTS</span></span>

## <span data-ttu-id="b7910-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b7910-125">NOTES</span></span>

## <span data-ttu-id="b7910-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b7910-126">RELATED LINKS</span></span>

[<span data-ttu-id="b7910-127">Get-AzureRmRecoveryServicesBackupManagementServer</span><span class="sxs-lookup"><span data-stu-id="b7910-127">Get-AzureRmRecoveryServicesBackupManagementServer</span></span>](./Get-AzureRmRecoveryServicesBackupManagementServer.md)


