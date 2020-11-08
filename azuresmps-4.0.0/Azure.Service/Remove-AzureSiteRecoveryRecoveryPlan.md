---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: A62D8097-FC26-40E4-803C-09F7979A2A2B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 91f96e5004446a4490a1d9b78a2dc0c7f3a25cd6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106111"
---
# <span data-ttu-id="fe1e6-101">Remove-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fe1e6-101">Remove-AzureSiteRecoveryRecoveryPlan</span></span>

## <span data-ttu-id="fe1e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe1e6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1e6-103">Site kurtarma planını site kurtarmadan kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-103">Removes a site recovery plan from Site Recovery.</span></span>

## <span data-ttu-id="fe1e6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fe1e6-104">SYNTAX</span></span>

### <span data-ttu-id="fe1e6-105">ByRPObject (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="fe1e6-105">ByRPObject (Default)</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan <ASRRecoveryPlan> [-WaitForCompletion] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe1e6-106">Byıd</span><span class="sxs-lookup"><span data-stu-id="fe1e6-106">ById</span></span>
```
Remove-AzureSiteRecoveryRecoveryPlan -Id <String> [-WaitForCompletion] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe1e6-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="fe1e6-107">DESCRIPTION</span></span>
<span data-ttu-id="fe1e6-108">**Remove-AzureSiteRecoveryRecoveryPlan** cmdlet 'ı geçerli Azure Site Recovery 'den bir site kurtarma planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-108">The **Remove-AzureSiteRecoveryRecoveryPlan** cmdlet removes a site recovery plan from the current Azure Site Recovery.</span></span>

## <span data-ttu-id="fe1e6-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fe1e6-109">EXAMPLES</span></span>

### <span data-ttu-id="fe1e6-110">Örnek 1: kurtarma planını kaldırma</span><span class="sxs-lookup"><span data-stu-id="fe1e6-110">Example 1: Remove a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Remove-AzureSiteRecoveryRecoveryPlan -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="fe1e6-111">İlk komut **Get-AzureSiteRecoveryRecoveryPlan** cmdlet 'Ini kullanarak site kurtarma planını alır ve $RecoveryPlan değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-111">The first command uses the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet to get the Site Recovery plan, and then stores it in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="fe1e6-112">İkinci komut $RecoveryPlan 'da kurtarma planını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-112">The second command removes the recovery plan in $RecoveryPlan.</span></span>

## <span data-ttu-id="fe1e6-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fe1e6-113">PARAMETERS</span></span>

### <span data-ttu-id="fe1e6-114">-Force</span><span class="sxs-lookup"><span data-stu-id="fe1e6-114">-Force</span></span>
<span data-ttu-id="fe1e6-115">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-115">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1e6-116">-ID</span><span class="sxs-lookup"><span data-stu-id="fe1e6-116">-Id</span></span>
<span data-ttu-id="fe1e6-117">Kaldırılacak kurtarma planının KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-117">Specifies the ID of the recovery plan to remove.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1e6-118">-Profil</span><span class="sxs-lookup"><span data-stu-id="fe1e6-118">-Profile</span></span>
<span data-ttu-id="fe1e6-119">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fe1e6-120">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1e6-121">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fe1e6-121">-RecoveryPlan</span></span>
<span data-ttu-id="fe1e6-122">Kaldırılacak kurtarma planını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-122">Specifies the recovery plan to remove.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe1e6-123">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="fe1e6-123">-WaitForCompletion</span></span>
<span data-ttu-id="fe1e6-124">Cmdlet 'in denetimi Windows PowerShell konsoluna göndermeden önce işlemin tamamlanmasını beklediğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-124">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1e6-125">-Onay</span><span class="sxs-lookup"><span data-stu-id="fe1e6-125">-Confirm</span></span>
<span data-ttu-id="fe1e6-126">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1e6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe1e6-127">-WhatIf</span></span>
<span data-ttu-id="fe1e6-128">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe1e6-129">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1e6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1e6-130">CommonParameters</span></span>
<span data-ttu-id="fe1e6-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fe1e6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1e6-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1e6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1e6-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fe1e6-133">INPUTS</span></span>

## <span data-ttu-id="fe1e6-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fe1e6-134">OUTPUTS</span></span>

## <span data-ttu-id="fe1e6-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fe1e6-135">NOTES</span></span>

## <span data-ttu-id="fe1e6-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fe1e6-136">RELATED LINKS</span></span>

[<span data-ttu-id="fe1e6-137">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fe1e6-137">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="fe1e6-138">New-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fe1e6-138">New-AzureSiteRecoveryRecoveryPlan</span></span>](./New-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="fe1e6-139">Güncelleştirme-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="fe1e6-139">Update-AzureSiteRecoveryRecoveryPlan</span></span>](./Update-AzureSiteRecoveryRecoveryPlan.md)


