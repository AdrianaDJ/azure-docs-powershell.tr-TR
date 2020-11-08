---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106241"
---
# <span data-ttu-id="0b888-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="0b888-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="0b888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b888-102">SYNOPSIS</span></span>
<span data-ttu-id="0b888-103">Yol tablosunu Azure Resource Manager yığınına geçirir.</span><span class="sxs-lookup"><span data-stu-id="0b888-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="0b888-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0b888-104">SYNTAX</span></span>

### <span data-ttu-id="0b888-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b888-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b888-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b888-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b888-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b888-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b888-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b888-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b888-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="0b888-109">DESCRIPTION</span></span>
<span data-ttu-id="0b888-110">**Taşıma-AzureRouteTable** cmdlet 'i, yol tablosunu Azure Kaynak Yöneticisi yığınındaki bir kaynak grubuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="0b888-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="0b888-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0b888-111">EXAMPLES</span></span>

### <span data-ttu-id="0b888-112">2</span><span class="sxs-lookup"><span data-stu-id="0b888-112">1:</span></span>
```

```

## <span data-ttu-id="0b888-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0b888-113">PARAMETERS</span></span>

### <span data-ttu-id="0b888-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="0b888-114">-Abort</span></span>
<span data-ttu-id="0b888-115">Bu cmdlet 'in yol tablosu geçişini iptal ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b888-115">Indicates that this cmdlet cancels the route table migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b888-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="0b888-116">-Commit</span></span>
<span data-ttu-id="0b888-117">Bu cmdlet 'in yol tablosu geçişini başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b888-117">Indicates that this cmdlet starts the route table migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b888-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="0b888-118">-InformationAction</span></span>
<span data-ttu-id="0b888-119">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b888-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0b888-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="0b888-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b888-121">'A</span><span class="sxs-lookup"><span data-stu-id="0b888-121">Continue</span></span>
- <span data-ttu-id="0b888-122">Manıza</span><span class="sxs-lookup"><span data-stu-id="0b888-122">Ignore</span></span>
- <span data-ttu-id="0b888-123">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="0b888-123">Inquire</span></span>
- <span data-ttu-id="0b888-124">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="0b888-124">SilentlyContinue</span></span>
- <span data-ttu-id="0b888-125">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="0b888-125">Stop</span></span>
- <span data-ttu-id="0b888-126">Biliriz</span><span class="sxs-lookup"><span data-stu-id="0b888-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b888-127">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="0b888-127">-InformationVariable</span></span>
<span data-ttu-id="0b888-128">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b888-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b888-129">-Prepare</span><span class="sxs-lookup"><span data-stu-id="0b888-129">-Prepare</span></span>
<span data-ttu-id="0b888-130">Bu cmdlet 'in yol tablosunu geçiş için hazırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b888-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b888-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="0b888-131">-Profile</span></span>
<span data-ttu-id="0b888-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b888-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b888-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="0b888-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b888-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="0b888-134">-RouteTableName</span></span>
<span data-ttu-id="0b888-135">Bu cmdlet 'in geçirolduğu yol tablosunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b888-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b888-136">-Doğrulama</span><span class="sxs-lookup"><span data-stu-id="0b888-136">-Validate</span></span>
<span data-ttu-id="0b888-137">Bu cmdlet 'in geçiş için yol tablosunu doğrulayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="0b888-137">Specifies that this cmdlet validates the route table for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b888-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="0b888-138">-Confirm</span></span>
<span data-ttu-id="0b888-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0b888-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b888-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b888-140">-WhatIf</span></span>
<span data-ttu-id="0b888-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0b888-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b888-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0b888-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b888-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b888-143">CommonParameters</span></span>
<span data-ttu-id="0b888-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0b888-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b888-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b888-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b888-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0b888-146">INPUTS</span></span>

## <span data-ttu-id="0b888-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0b888-147">OUTPUTS</span></span>

## <span data-ttu-id="0b888-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0b888-148">NOTES</span></span>

## <span data-ttu-id="0b888-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0b888-149">RELATED LINKS</span></span>

[<span data-ttu-id="0b888-150">Taşı-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="0b888-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="0b888-151">Taşı-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="0b888-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="0b888-152">Taşı-AzureService</span><span class="sxs-lookup"><span data-stu-id="0b888-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="0b888-153">Taşı-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="0b888-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="0b888-154">Taşı-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0b888-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


