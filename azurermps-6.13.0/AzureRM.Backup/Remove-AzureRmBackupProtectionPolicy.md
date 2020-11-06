---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 189E3DD8-AA43-4D4C-A873-971E0585E54E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/remove-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Remove-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: b7eaa3ef0c0379a0799e4091a4e808415b2f9fdc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588608"
---
# <span data-ttu-id="c3e1c-101">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3e1c-101">Remove-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="c3e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e1c-103">Yedek kasasından ilke siler.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-103">Deletes a policy from a Backup vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3e1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c3e1c-104">SYNTAX</span></span>

```
Remove-AzureRmBackupProtectionPolicy [-Force] [-ProtectionPolicy] <AzureRMBackupProtectionPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3e1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c3e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e1c-106">**Remove-AzureRmBackupProtectionPolicy** cmdlet 'i, bir Azure yedekleme kasasından ilke siler.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-106">The **Remove-AzureRmBackupProtectionPolicy** cmdlet deletes a policy from an Azure Backup vault.</span></span>
<span data-ttu-id="c3e1c-107">Yedekleme koruma ilkesini silebilmeniz için, ilkenin ilişkili yedekleme öğeleri olmaması gerekir.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-107">Before you can delete a backup protection policy, the policy must not have any associated Backup items.</span></span>
<span data-ttu-id="c3e1c-108">İlkeyi silmeden önce, her ilişkili öğenin başka bir ilkeyle ilişkilendirildiğinden emin olun.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-108">Before you delete the policy, make sure that each associated item is associated with some other policy.</span></span>
<span data-ttu-id="c3e1c-109">Başka bir ilkeyi yedekleme öğesiyle ilişkilendirmek için Enable-AzureRmBackupProtection cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-109">To associate another policy with a backup item, use the Enable-AzureRmBackupProtection cmdlet.</span></span>

## <span data-ttu-id="c3e1c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c3e1c-110">EXAMPLES</span></span>

### <span data-ttu-id="c3e1c-111">Örnek 1: yedekleme koruma ilkesini kaldırma</span><span class="sxs-lookup"><span data-stu-id="c3e1c-111">Example 1: Remove a backup protection policy</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupProtectionPolicy -Vault $Vault -Name "DailyBackup" | Remove-AzureRmBackupProtectionPolicy
```

<span data-ttu-id="c3e1c-112">İlk komut, Get-AzureRmBackupVault cmdlet 'ini kullanarak Vault03 adındaki kasayı alır.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-112">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="c3e1c-113">Komut bu nesneyi $Vault değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-113">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="c3e1c-114">İkinci komut 30 günlük bekletmenin bir bekletme ilkesi oluşturur ve ardından $Daily değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-114">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="c3e1c-115">İkinci komut, **Get-AzureRmBackupProtectionPolicy** cmdlet 'ini kullanarak $Vault kasada dailybackup adlı koruma ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-115">The second command gets the protection policy named DailyBackup in the vault in $Vault by using the **Get-AzureRmBackupProtectionPolicy** cmdlet.</span></span>
<span data-ttu-id="c3e1c-116">Komut ilkeyi geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-116">The command passes the policy to the current cmdlet.</span></span>
<span data-ttu-id="c3e1c-117">Bu cmdlet ilkeyi kaldırır.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-117">That cmdlet removes the policy.</span></span>

## <span data-ttu-id="c3e1c-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c3e1c-118">PARAMETERS</span></span>

### <span data-ttu-id="c3e1c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e1c-119">-DefaultProfile</span></span>
<span data-ttu-id="c3e1c-120">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c3e1c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c3e1c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c3e1c-121">-Force</span></span>
<span data-ttu-id="c3e1c-122">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c3e1c-123">-ProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3e1c-123">-ProtectionPolicy</span></span>
<span data-ttu-id="c3e1c-124">Bu cmdlet 'in kaldırdığı koruma ilkesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-124">Specifies protection policy that this cmdlet removes.</span></span>
<span data-ttu-id="c3e1c-125">**Azurermbackupprotectionpolicy** almak için Get-AzureRmBackupProtectionPolicy cmdlet 'ini kullanma</span><span class="sxs-lookup"><span data-stu-id="c3e1c-125">To obtain an **AzureRmBackupProtectionPolicy** , use the Get-AzureRmBackupProtectionPolicy cmdlet</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3e1c-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="c3e1c-126">-Confirm</span></span>
<span data-ttu-id="c3e1c-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3e1c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3e1c-128">-WhatIf</span></span>
<span data-ttu-id="c3e1c-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3e1c-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3e1c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e1c-131">CommonParameters</span></span>
<span data-ttu-id="c3e1c-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c3e1c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e1c-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e1c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e1c-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c3e1c-134">INPUTS</span></span>

### <span data-ttu-id="c3e1c-135">Microsoft. Azure. Commands. AzureBackup. modeller. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3e1c-135">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>
<span data-ttu-id="c3e1c-136">Parametreler: ProtectionPolicy (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c3e1c-136">Parameters: ProtectionPolicy (ByValue)</span></span>

## <span data-ttu-id="c3e1c-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c3e1c-137">OUTPUTS</span></span>

### <span data-ttu-id="c3e1c-138">System. void</span><span class="sxs-lookup"><span data-stu-id="c3e1c-138">System.Void</span></span>

## <span data-ttu-id="c3e1c-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c3e1c-139">NOTES</span></span>

## <span data-ttu-id="c3e1c-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c3e1c-140">RELATED LINKS</span></span>

[<span data-ttu-id="c3e1c-141">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c3e1c-141">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="c3e1c-142">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3e1c-142">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="c3e1c-143">Yeni-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c3e1c-143">New-AzureRmBackupProtectionPolicy</span></span>](./New-AzureRmBackupProtectionPolicy.md)


