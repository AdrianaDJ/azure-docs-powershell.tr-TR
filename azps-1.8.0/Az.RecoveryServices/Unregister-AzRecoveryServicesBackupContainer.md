---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A10DC2A2-A732-416F-9C68-6533C143AE8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/unregister-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Unregister-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: 410d78df47a37daa90213056170c86f24c423986
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93759583"
---
# <span data-ttu-id="0a25f-101">Unregister-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0a25f-101">Unregister-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="0a25f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a25f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a25f-103">Bir Windows sunucusunun veya başka bir kapsayıcının kasasından kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="0a25f-103">Unregisters a Windows Server or other container from the vault.</span></span>

## <span data-ttu-id="0a25f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a25f-104">SYNTAX</span></span>

```
Unregister-AzRecoveryServicesBackupContainer [-Container] <ContainerBase> [-PassThru] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a25f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a25f-105">DESCRIPTION</span></span>
<span data-ttu-id="0a25f-106">**Unregister-AzRecoveryServicesBackupContainer** cmdlet 'i, kasadan Windows sunucusunun veya diğer yedekleme kapsayıcısının kaydını siler.</span><span class="sxs-lookup"><span data-stu-id="0a25f-106">The **Unregister-AzRecoveryServicesBackupContainer** cmdlet unregisters a Windows Server or other Backup container from the vault.</span></span>
<span data-ttu-id="0a25f-107">Bu cmdlet, kasadaki bir kapsayıcıya yapılan başvuruları kaldırır.</span><span class="sxs-lookup"><span data-stu-id="0a25f-107">This cmdlet removes references to a container from the vault.</span></span>
<span data-ttu-id="0a25f-108">Bir kapsayıcının kaydını silebilmek için, bu kapsayıcıyla ilişkili tüm korumalı verileri silmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="0a25f-108">Before you can unregister a container, you must delete any protected data associated with that container.</span></span>
<span data-ttu-id="0a25f-109">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="0a25f-109">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0a25f-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a25f-110">EXAMPLES</span></span>

### <span data-ttu-id="0a25f-111">Örnek 1: kasadan bir Windows sunucusunun kaydını kaldırma</span><span class="sxs-lookup"><span data-stu-id="0a25f-111">Example 1: Unregister a Windows Server from the vault</span></span>
```
PS C:\>$Cont = Get-AzRecoveryServicesBackupContainer -ContainerType "Windows" -BackupManagementType MARS -Name "server01.contoso.com"
PS C:\> Unregister-AzRecoveryServicesBackupContainer -Container $Cont
```

<span data-ttu-id="0a25f-112">İlk komut, kasaya kaydedilen server01.contoso.com adındaki Windows kapsayıcısını alır ve $Cont değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0a25f-112">The first command gets the Windows container named server01.contoso.com that is registered in the vault, and then stores it in the $Cont variable.</span></span>
<span data-ttu-id="0a25f-113">İkinci komut belirtilen Windows sunucusunun kaydını Azure yedekleme kasasından siler.</span><span class="sxs-lookup"><span data-stu-id="0a25f-113">The second command unregisters the specified Windows Server from the Azure Backup vault.</span></span>

## <span data-ttu-id="0a25f-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a25f-114">PARAMETERS</span></span>

### <span data-ttu-id="0a25f-115">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="0a25f-115">-Container</span></span>
<span data-ttu-id="0a25f-116">Kaydı kaldırmak için bir yedekleme kapsayıcısı nesnesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="0a25f-116">Specifies a Backup container object to unregister.</span></span>
<span data-ttu-id="0a25f-117">**Backupcontainer** nesnesi almak için Get-AzRecoveryServicesBackupContainer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="0a25f-117">To obtain a **BackupContainer** object, use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a25f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a25f-118">-DefaultProfile</span></span>
<span data-ttu-id="0a25f-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0a25f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a25f-120">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="0a25f-120">-PassThru</span></span>
<span data-ttu-id="0a25f-121">Silinecek kapsayıcıyı döndürün.</span><span class="sxs-lookup"><span data-stu-id="0a25f-121">Return the container to be deleted.</span></span>

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

### <span data-ttu-id="0a25f-122">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0a25f-122">-VaultId</span></span>
<span data-ttu-id="0a25f-123">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0a25f-123">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0a25f-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a25f-124">-Confirm</span></span>
<span data-ttu-id="0a25f-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a25f-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a25f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a25f-126">-WhatIf</span></span>
<span data-ttu-id="0a25f-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a25f-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a25f-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0a25f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a25f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a25f-129">CommonParameters</span></span>
<span data-ttu-id="0a25f-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a25f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a25f-131">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a25f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a25f-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a25f-132">INPUTS</span></span>

### <span data-ttu-id="0a25f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0a25f-133">System.String</span></span>

## <span data-ttu-id="0a25f-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a25f-134">OUTPUTS</span></span>

### <span data-ttu-id="0a25f-135">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="0a25f-135">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="0a25f-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a25f-136">NOTES</span></span>

## <span data-ttu-id="0a25f-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a25f-137">RELATED LINKS</span></span>

[<span data-ttu-id="0a25f-138">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="0a25f-138">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)


