---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: BFE741CC-C166-4534-93F4-D21AAFAD9FF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesBackupProtectionPolicy.md
ms.openlocfilehash: c3f4bb9b7c3d2b862ff78fdb35517f5837ffedf0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94278025"
---
# <span data-ttu-id="de87d-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="de87d-101">Remove-AzRecoveryServicesBackupProtectionPolicy</span></span>

## <span data-ttu-id="de87d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de87d-102">SYNOPSIS</span></span>
<span data-ttu-id="de87d-103">Bir kasadan yedek koruma ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="de87d-103">Deletes a Backup protection policy from a vault.</span></span>

## <span data-ttu-id="de87d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="de87d-104">SYNTAX</span></span>

### <span data-ttu-id="de87d-105">PolicyName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="de87d-105">PolicyName (Default)</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Name] <String> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de87d-106">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="de87d-106">PolicyObject</span></span>
```
Remove-AzRecoveryServicesBackupProtectionPolicy [-Policy] <PolicyBase> [-PassThru] [-Force] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de87d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="de87d-107">DESCRIPTION</span></span>
<span data-ttu-id="de87d-108">**Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet 'inin yedekleme ilkelerini siler.</span><span class="sxs-lookup"><span data-stu-id="de87d-108">The **Remove-AzRecoveryServicesBackupProtectionPolicy** cmdlet deletes backup policies for a vault.</span></span>
<span data-ttu-id="de87d-109">Yedekleme koruma ilkesini silebilmeniz için, ilkenin ilişkili yedekleme öğeleri olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="de87d-109">Before you can delete a Backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="de87d-110">İlkeyi silmeden önce, her ilişkili öğenin başka bir ilkeyle ilişkilendirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="de87d-110">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="de87d-111">Başka bir ilkeyi yedekleme öğesiyle ilişkilendirmek için Enable-AzRecoveryServicesBackupProtection cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="de87d-111">To associate another policy with a Backup item, use the Enable-AzRecoveryServicesBackupProtection cmdlet.</span></span>
<span data-ttu-id="de87d-112">Geçerli cmdlet 'i kullanmadan önce Set-AzRecoveryServicesVaultContext cmdlet 'ini kullanarak kasa bağlamını ayarlayın.</span><span class="sxs-lookup"><span data-stu-id="de87d-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="de87d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="de87d-113">EXAMPLES</span></span>

### <span data-ttu-id="de87d-114">Örnek 1: ilkeyi kaldırma</span><span class="sxs-lookup"><span data-stu-id="de87d-114">Example 1: Remove a policy</span></span>
```powershell
PS C:\>$Pol= Get-AzRecoveryServicesBackupProtectionPolicy -Name "NewPolicy"
PS C:\> Remove-AzRecoveryServicesBackupProtectionPolicy -Policy $Pol
```

<span data-ttu-id="de87d-115">İlk komut NewPolicy adındaki yedekleme koruma ilkesini alır ve $Pol değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="de87d-115">The first command gets the Backup protection policy named NewPolicy, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="de87d-116">İkinci komut $Pol ilke nesnesini kaldırır.</span><span class="sxs-lookup"><span data-stu-id="de87d-116">The second command removes the policy object in $Pol.</span></span>

### <span data-ttu-id="de87d-117">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="de87d-117">Example 2</span></span>

<span data-ttu-id="de87d-118">Bir kasadan yedek koruma ilkesini siler.</span><span class="sxs-lookup"><span data-stu-id="de87d-118">Deletes a Backup protection policy from a vault.</span></span> <span data-ttu-id="de87d-119">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="de87d-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzRecoveryServicesBackupProtectionPolicy -Name 'V2VM' -VaultId $vault.ID
```

## <span data-ttu-id="de87d-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="de87d-120">PARAMETERS</span></span>

### <span data-ttu-id="de87d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de87d-121">-DefaultProfile</span></span>
<span data-ttu-id="de87d-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="de87d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de87d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="de87d-123">-Force</span></span>
<span data-ttu-id="de87d-124">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="de87d-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="de87d-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="de87d-125">-Name</span></span>
<span data-ttu-id="de87d-126">Kaldırılacak yedekleme koruması ilkesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="de87d-126">Specifies the name of the Backup protection policy to remove.</span></span>

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

### <span data-ttu-id="de87d-127">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="de87d-127">-PassThru</span></span>
<span data-ttu-id="de87d-128">Silinecek ilkeyi döndür.</span><span class="sxs-lookup"><span data-stu-id="de87d-128">Return the policy to be deleted.</span></span>

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

### <span data-ttu-id="de87d-129">-İlke</span><span class="sxs-lookup"><span data-stu-id="de87d-129">-Policy</span></span>
<span data-ttu-id="de87d-130">Kaldırılacak yedekleme koruması ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="de87d-130">Specifies the Backup protection policy to remove.</span></span>
<span data-ttu-id="de87d-131">**Yedeklemeilkesi** nesnesi almak için Get-AzRecoveryServicesBackupProtectionPolicy cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="de87d-131">To obtain an **BackupPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="de87d-132">-VaultId</span><span class="sxs-lookup"><span data-stu-id="de87d-132">-VaultId</span></span>
<span data-ttu-id="de87d-133">Kurtarma Hizmetleri kasasındaki ARM KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="de87d-133">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="de87d-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="de87d-134">-Confirm</span></span>
<span data-ttu-id="de87d-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="de87d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de87d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de87d-136">-WhatIf</span></span>
<span data-ttu-id="de87d-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="de87d-137">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="de87d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de87d-138">CommonParameters</span></span>
<span data-ttu-id="de87d-139">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="de87d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de87d-140">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="de87d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de87d-141">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="de87d-141">INPUTS</span></span>

### <span data-ttu-id="de87d-142">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="de87d-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

### <span data-ttu-id="de87d-143">System. String</span><span class="sxs-lookup"><span data-stu-id="de87d-143">System.String</span></span>

## <span data-ttu-id="de87d-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="de87d-144">OUTPUTS</span></span>

### <span data-ttu-id="de87d-145">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlet. model. PolicyBase</span><span class="sxs-lookup"><span data-stu-id="de87d-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase</span></span>

## <span data-ttu-id="de87d-146">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="de87d-146">NOTES</span></span>

## <span data-ttu-id="de87d-147">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="de87d-147">RELATED LINKS</span></span>

[<span data-ttu-id="de87d-148">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="de87d-148">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="de87d-149">New-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="de87d-149">New-AzRecoveryServicesBackupProtectionPolicy</span></span>](./New-AzRecoveryServicesBackupProtectionPolicy.md)

[<span data-ttu-id="de87d-150">Set-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="de87d-150">Set-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Set-AzRecoveryServicesBackupProtectionPolicy.md)


