---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35b937b810da65cc3cc2ed330198011ec108f9d6
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2020
ms.locfileid: "93938572"
---
# <span data-ttu-id="875d1-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="875d1-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="875d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="875d1-102">SYNOPSIS</span></span>
<span data-ttu-id="875d1-103">Yedeği geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="875d1-103">Restore a backup.</span></span>

## <span data-ttu-id="875d1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="875d1-104">SYNTAX</span></span>

### <span data-ttu-id="875d1-105">Backups_Restore (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="875d1-105">Backups_Restore (Default)</span></span>
```
Restore-AzsBackup [-ResourceGroupName <String>] -Name <String> [-Location <String>]
 -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="875d1-106">Içermiyor</span><span class="sxs-lookup"><span data-stu-id="875d1-106">ResourceId</span></span>
```
Restore-AzsBackup -DecryptionCertPath <String> -DecryptionCertPassword <SecureString> -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="875d1-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="875d1-107">DESCRIPTION</span></span>
<span data-ttu-id="875d1-108">Yedeği geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="875d1-108">Restore a backup.</span></span>

## <span data-ttu-id="875d1-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="875d1-109">EXAMPLES</span></span>

### <span data-ttu-id="875d1-110">ÖRNEK 1</span><span class="sxs-lookup"><span data-stu-id="875d1-110">EXAMPLE 1</span></span>
```
Restore-AzsBackup -Name 4e90bd2f-c7ab-47a3-a3c7-908cddd1ad0e -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword
```

<span data-ttu-id="875d1-111">Azure yığın yedeklemesinden geri yükleme.</span><span class="sxs-lookup"><span data-stu-id="875d1-111">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="875d1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="875d1-112">PARAMETERS</span></span>

### <span data-ttu-id="875d1-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="875d1-113">-AsJob</span></span>
<span data-ttu-id="875d1-114">Zaman uyumsuz bir iş olarak çalıştırıp iş nesnesini döndürün.</span><span class="sxs-lookup"><span data-stu-id="875d1-114">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875d1-115">-Şifre \ parola</span><span class="sxs-lookup"><span data-stu-id="875d1-115">-DecryptionCertPassword</span></span>
<span data-ttu-id="875d1-116">Şifre çözme sertifikası parolası.</span><span class="sxs-lookup"><span data-stu-id="875d1-116">Password of the decryption cert.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875d1-117">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="875d1-117">-DecryptionCertPath</span></span>
<span data-ttu-id="875d1-118">Özel anahtarı (. pfx) içeren şifre çözme sertifikası dosyasının yolu.</span><span class="sxs-lookup"><span data-stu-id="875d1-118">Path to the decryption cert file with private key (.pfx).</span></span>

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

### <span data-ttu-id="875d1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="875d1-119">-Force</span></span>
<span data-ttu-id="875d1-120">Onayınızı sorma.</span><span class="sxs-lookup"><span data-stu-id="875d1-120">Don't ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875d1-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="875d1-121">-Location</span></span>
<span data-ttu-id="875d1-122">Yedeklenecek yerin adı.</span><span class="sxs-lookup"><span data-stu-id="875d1-122">Name of location to backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875d1-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="875d1-123">-Name</span></span>
<span data-ttu-id="875d1-124">Yedeğin adı.</span><span class="sxs-lookup"><span data-stu-id="875d1-124">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875d1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="875d1-125">-ResourceGroupName</span></span>
<span data-ttu-id="875d1-126">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="875d1-126">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Backups_Restore
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="875d1-127">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="875d1-127">-ResourceId</span></span>
<span data-ttu-id="875d1-128">Kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="875d1-128">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="875d1-129">-Onay</span><span class="sxs-lookup"><span data-stu-id="875d1-129">-Confirm</span></span>
<span data-ttu-id="875d1-130">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="875d1-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="875d1-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="875d1-131">-WhatIf</span></span>
<span data-ttu-id="875d1-132">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="875d1-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="875d1-133">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="875d1-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="875d1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="875d1-134">CommonParameters</span></span>
<span data-ttu-id="875d1-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="875d1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="875d1-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="875d1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="875d1-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="875d1-137">INPUTS</span></span>

## <span data-ttu-id="875d1-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="875d1-138">OUTPUTS</span></span>

## <span data-ttu-id="875d1-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="875d1-139">NOTES</span></span>

## <span data-ttu-id="875d1-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="875d1-140">RELATED LINKS</span></span>
