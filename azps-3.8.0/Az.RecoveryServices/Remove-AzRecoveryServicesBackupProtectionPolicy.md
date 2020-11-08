---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: 775d3349d0bb9392ad51a260a478c45c13163008
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103542"
---
# <span data-ttu-id="59ec6-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59ec6-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="59ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="59ec6-103">Bir kasadan yedek koruma ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="59ec6-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="59ec6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="59ec6-104">SYNTAX</span></span>

### <span data-ttu-id="59ec6-105">PolicyName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="59ec6-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59ec6-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="59ec6-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59ec6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="59ec6-107">DESCRIPTION</span></span>
<span data-ttu-id="59ec6-108">**Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet 'inin yedekleme ilkelerini siler.</span><span class="sxs-lookup"><span data-stu-id="59ec6-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="59ec6-109">Yedekleme koruma ilkesini silebilmeniz için, ilkenin ilişkili yedekleme öğeleri olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="59ec6-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="59ec6-110">İlkeyi silmeden önce, her ilişkili öğenin başka bir ilkeyle ilişkilendirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="59ec6-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="59ec6-111">Başka bir ilkeyi yedekleme öğesiyle ilişkilendirmek için Enable-AzRecoveryServicesBackupProtection cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="59ec6-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="59ec6-112">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="59ec6-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="59ec6-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="59ec6-113">EXAMPLES</span></span>

### <span data-ttu-id="59ec6-114">Örnek 1: ilkeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="59ec6-114">Example 1: Remove a policy</span></span>
```
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="59ec6-115">İlk komut NewPolicy adındaki yedekleme koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="59ec6-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="59ec6-116">İkinci komut $Pol ilke nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="59ec6-116">The second command removes the policy object in $Pol.</span></span>

## <span data-ttu-id="59ec6-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="59ec6-117">PARAMETERS</span></span>

### <span data-ttu-id="59ec6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59ec6-118">-DefaultProfile</span></span>
<span data-ttu-id="59ec6-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="59ec6-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59ec6-120">-Force</span><span class="sxs-lookup"><span data-stu-id="59ec6-120">-Force</span></span>
<span data-ttu-id="59ec6-121">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="59ec6-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="59ec6-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="59ec6-122">-Name</span></span>
<span data-ttu-id="59ec6-123">Kaldırılacak yedekleme koruması ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="59ec6-123">Specifies the name of the Backup protection policy to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ec6-124">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="59ec6-124">-PassThru</span></span>
<span data-ttu-id="59ec6-125">Silinecek ilkeyi döndür.</span><span class="sxs-lookup"><span data-stu-id="59ec6-125">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="59ec6-126">-İlke</span><span class="sxs-lookup"><span data-stu-id="59ec6-126">-Policy</span></span>
<span data-ttu-id="59ec6-127">Kaldırılacak yedekleme koruması ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="59ec6-127">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="59ec6-128">**Yedeklemeilkesi** nesnesi almak için Get-AzRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="59ec6-128">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: PolicyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="59ec6-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="59ec6-129">-VaultId</span></span>
<span data-ttu-id="59ec6-130">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="59ec6-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="59ec6-131">-Onay</span><span class="sxs-lookup"><span data-stu-id="59ec6-131">-Confirm</span></span>
<span data-ttu-id="59ec6-132">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="59ec6-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ec6-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59ec6-133">-WhatIf</span></span>
<span data-ttu-id="59ec6-134">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="59ec6-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59ec6-135">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="59ec6-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59ec6-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59ec6-136">CommonParameters</span></span>
<span data-ttu-id="59ec6-137">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="59ec6-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59ec6-138">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="59ec6-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59ec6-139">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="59ec6-139">INPUTS</span></span>

### <span data-ttu-id="59ec6-140">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="59ec6-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="59ec6-141">System. String</span><span class="sxs-lookup"><span data-stu-id="59ec6-141">System.String</span></span>

## <span data-ttu-id="59ec6-142">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="59ec6-142">OUTPUTS</span></span>

### <span data-ttu-id="59ec6-143">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="59ec6-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="59ec6-144">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="59ec6-144">NOTES</span></span>

## <span data-ttu-id="59ec6-145">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="59ec6-145">RELATED LINKS</span></span>

[<span data-ttu-id="59ec6-146">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59ec6-146">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="59ec6-147">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59ec6-147">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="59ec6-148">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="59ec6-148">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


