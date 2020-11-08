---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/register-azrecoveryservicesbackupcontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Register-AzRecoveryServicesBackupContainer.md
ms.openlocfilehash: a6c47561b8fdb9e748940c917d85548d25be1ccf
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098160"
---
# <span data-ttu-id="bf9f1-101">Register-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="bf9f1-101">Register-AzRecoveryServicesBackupContainer</span></span>

## <span data-ttu-id="bf9f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf9f1-102">SYNOPSIS</span></span>
<span data-ttu-id="bf9f1-103">Bu komut, Azure Backup 'ın kaynağı, söz konusu kurtarma hizmetleri kasasına kaydedilen bir yedek kapsayıcıya dönüştürmesini sağlar.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-103">This command allows Azure Backup to convert the �Resource� to a �Backup Container� which is then registered to the given Recovery services vault.</span></span> <span data-ttu-id="bf9f1-104">Azure yedekleme hizmeti daha sonra bu kapsayıcıdaki belirli iş yükü türünün iş yüklerini daha sonra korunabilir şekilde bulabilir.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-104">The Azure Backup service can then discover workloads of the given workload type within this container to be protected later.</span></span>

## <span data-ttu-id="bf9f1-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bf9f1-105">SYNTAX</span></span>

### <span data-ttu-id="bf9f1-106">Kaydet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bf9f1-106">Register (Default)</span></span>
```
Register-AzRecoveryServicesBackupContainer [-ResourceId] <String>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf9f1-107">Diğiniz</span><span class="sxs-lookup"><span data-stu-id="bf9f1-107">ReRegister</span></span>
```
Register-AzRecoveryServicesBackupContainer [-Container] <ContainerBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf9f1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bf9f1-108">DESCRIPTION</span></span>
<span data-ttu-id="bf9f1-109">Cmdlet, belirli workloadType ile AzureWorkloads için bir Azure VM kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-109">The cmdlet registers an Azure VM for AzureWorkloads with specific workloadType.</span></span>

## <span data-ttu-id="bf9f1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bf9f1-110">EXAMPLES</span></span>

### <span data-ttu-id="bf9f1-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="bf9f1-111">Example 1</span></span>
```
PS C:\> Register-AzRecoveryServicesBackupContainer -ResourceId <AzureVMID> -VaultId <vaultID> -WorkloadType �MSSQL� -BackupManagementType �AzureWorkload�
```

<span data-ttu-id="bf9f1-112">Cmdlet, iş yükü MSSQL için bir Azure VM kaydeder.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-112">The cmdlet registers an azure VM for the workload MSSQL.</span></span>

## <span data-ttu-id="bf9f1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bf9f1-113">PARAMETERS</span></span>

### <span data-ttu-id="bf9f1-114">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="bf9f1-114">-BackupManagementType</span></span>
<span data-ttu-id="bf9f1-115">Azure yedekleme kapsayıcısının yedekleme yönetimi türü</span><span class="sxs-lookup"><span data-stu-id="bf9f1-115">The backup management type of the Azure Backup container</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9f1-116">Kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="bf9f1-116">-Container</span></span>
<span data-ttu-id="bf9f1-117">Öğenin bulunduğu kapsayıcı</span><span class="sxs-lookup"><span data-stu-id="bf9f1-117">Container where the item resides</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: ReRegister
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf9f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf9f1-118">-DefaultProfile</span></span>
<span data-ttu-id="bf9f1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf9f1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="bf9f1-120">-Force</span></span>
<span data-ttu-id="bf9f1-121">Kayıt kapsayıcısını zorunlu kılın (onay iletişim kutusu).</span><span class="sxs-lookup"><span data-stu-id="bf9f1-121">Force registers container (prevents confirmation dialog).</span></span> <span data-ttu-id="bf9f1-122">Bu parametre isteğe bağlıdır.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="bf9f1-123">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bf9f1-123">-ResourceId</span></span>
<span data-ttu-id="bf9f1-124">Abonelikteki bazı RecoveryServices Kasası tarafından zaten korunuyorsa, temsilci öğesinin denetlenmesi gereken Azure kaynağının KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-124">ID of the Azure Resource whose representative item needs to be checked if it is already protected by some RecoveryServices Vault in the subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Register
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9f1-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="bf9f1-125">-VaultId</span></span>
<span data-ttu-id="bf9f1-126">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="bf9f1-127">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="bf9f1-127">-WorkloadType</span></span>
<span data-ttu-id="bf9f1-128">Kaynağın iş yükü türü (örneğin: AzureVM, WindowsServer, AzureFiles, MSSQL).</span><span class="sxs-lookup"><span data-stu-id="bf9f1-128">Workload type of the resource (for example: AzureVM, WindowsServer, AzureFiles, MSSQL).</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf9f1-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="bf9f1-129">-Confirm</span></span>
<span data-ttu-id="bf9f1-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf9f1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf9f1-131">-WhatIf</span></span>
<span data-ttu-id="bf9f1-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf9f1-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf9f1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf9f1-134">CommonParameters</span></span>
<span data-ttu-id="bf9f1-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf9f1-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bf9f1-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf9f1-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bf9f1-137">INPUTS</span></span>

### <span data-ttu-id="bf9f1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="bf9f1-138">System.String</span></span>

## <span data-ttu-id="bf9f1-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bf9f1-139">OUTPUTS</span></span>

### <span data-ttu-id="bf9f1-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="bf9f1-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

## <span data-ttu-id="bf9f1-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bf9f1-141">NOTES</span></span>

## <span data-ttu-id="bf9f1-142">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bf9f1-142">RELATED LINKS</span></span>
