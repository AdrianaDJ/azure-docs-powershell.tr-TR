---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 6E886340-864C-4FF6-8FA3-669D637770F3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Disable-AzureRmBackupProtection.md
ms.openlocfilehash: e25cbbeb4f9920e468638bbae2ef8c53ca241fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762232"
---
# <span data-ttu-id="75c2f-101">Disable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="75c2f-101">Disable-AzureRmBackupProtection</span></span>

## <span data-ttu-id="75c2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75c2f-102">SYNOPSIS</span></span>
<span data-ttu-id="75c2f-103">Korumalı bir yedekleme öğesi için korumayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="75c2f-103">Disables protection for a Backup protected item.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75c2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="75c2f-104">SYNTAX</span></span>

```
Disable-AzureRmBackupProtection [-RemoveRecoveryPoints] [-Force] [-Item] <AzureRMBackupItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75c2f-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="75c2f-105">DESCRIPTION</span></span>
<span data-ttu-id="75c2f-106">**Disable-AzureRmBackupProtection** cmdlet 'ı Azure Backup korumalı öğesi için korumayı devre dışı bırakır.</span><span class="sxs-lookup"><span data-stu-id="75c2f-106">The **Disable-AzureRmBackupProtection** cmdlet disables protection for an Azure Backup protected item.</span></span>
<span data-ttu-id="75c2f-107">Bu cmdlet, bir öğenin olağan zamanlanmış yedeklemesini durdurur.</span><span class="sxs-lookup"><span data-stu-id="75c2f-107">This cmdlet stops regular scheduled backup of an item.</span></span>
<span data-ttu-id="75c2f-108">Bu cmdlet, yedekleme öğesi için var olan kurtarma noktalarını silebilir.</span><span class="sxs-lookup"><span data-stu-id="75c2f-108">This cmdlet can delete existing recovery points for the backup item.</span></span>

## <span data-ttu-id="75c2f-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="75c2f-109">EXAMPLES</span></span>

## <span data-ttu-id="75c2f-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="75c2f-110">PARAMETERS</span></span>

### <span data-ttu-id="75c2f-111">-Force</span><span class="sxs-lookup"><span data-stu-id="75c2f-111">-Force</span></span>
<span data-ttu-id="75c2f-112">Komutu Kullanıcı onayını istemeden çalıştırmaya zorlar.</span><span class="sxs-lookup"><span data-stu-id="75c2f-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75c2f-113">-Öğe</span><span class="sxs-lookup"><span data-stu-id="75c2f-113">-Item</span></span>
<span data-ttu-id="75c2f-114">Bu cmdlet 'in korumayı devre dışı bırakacağını belirten yedekleme öğesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c2f-114">Specifies the Backup item for which this cmdlet disables protection.</span></span>
<span data-ttu-id="75c2f-115">**Azurermbackupöğesi** almak için Get-AzureRmBackupItem cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="75c2f-115">To obtain an **AzureRmBackupItem** , use the Get-AzureRmBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75c2f-116">-RemoveRecoveryPoints</span><span class="sxs-lookup"><span data-stu-id="75c2f-116">-RemoveRecoveryPoints</span></span>
<span data-ttu-id="75c2f-117">Bu cmdlet 'in var olan kurtarma noktalarını sildiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="75c2f-117">Indicates that this cmdlet deletes existing recovery points.</span></span>
<span data-ttu-id="75c2f-118">Depolanan kurtarma noktalarını daha sonra silmek için, bu cmdlet 'i yeniden çalıştırın ve bu parametreyi belirtin.</span><span class="sxs-lookup"><span data-stu-id="75c2f-118">To delete stored recovery points later, run this cmdlet again and specify this parameter.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75c2f-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="75c2f-119">-Confirm</span></span>
<span data-ttu-id="75c2f-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="75c2f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75c2f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75c2f-121">-WhatIf</span></span>
<span data-ttu-id="75c2f-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="75c2f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75c2f-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="75c2f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75c2f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75c2f-124">-DefaultProfile</span></span>
<span data-ttu-id="75c2f-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="75c2f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75c2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75c2f-126">CommonParameters</span></span>
<span data-ttu-id="75c2f-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="75c2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75c2f-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75c2f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75c2f-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="75c2f-129">INPUTS</span></span>

### <span data-ttu-id="75c2f-130">Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="75c2f-130">AzureRmBackupItem</span></span>

## <span data-ttu-id="75c2f-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="75c2f-131">OUTPUTS</span></span>

### <span data-ttu-id="75c2f-132">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="75c2f-132">AzureRmBackupJob</span></span>

## <span data-ttu-id="75c2f-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="75c2f-133">NOTES</span></span>

## <span data-ttu-id="75c2f-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="75c2f-134">RELATED LINKS</span></span>

[<span data-ttu-id="75c2f-135">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="75c2f-135">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="75c2f-136">Get-Azurermbackupıtem</span><span class="sxs-lookup"><span data-stu-id="75c2f-136">Get-AzureRmBackupItem</span></span>](./Get-AzureRmBackupItem.md)


