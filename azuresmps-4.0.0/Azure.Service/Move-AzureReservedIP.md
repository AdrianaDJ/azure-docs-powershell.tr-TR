---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106242"
---
# <span data-ttu-id="46cd2-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="46cd2-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="46cd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46cd2-102">SYNOPSIS</span></span>
<span data-ttu-id="46cd2-103">Ayrılmış bir IP adresini Azure Resource Manager yığınına geçirir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="46cd2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="46cd2-104">SYNTAX</span></span>

### <span data-ttu-id="46cd2-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="46cd2-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46cd2-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="46cd2-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46cd2-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="46cd2-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="46cd2-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="46cd2-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46cd2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="46cd2-109">DESCRIPTION</span></span>
<span data-ttu-id="46cd2-110">**Taþý-AzureReservedIP** cmdlet 'i, BIR ayrılmış IP adresini Azure Resource Manager yığınındaki kaynak grubuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="46cd2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="46cd2-111">EXAMPLES</span></span>

### <span data-ttu-id="46cd2-112">2</span><span class="sxs-lookup"><span data-stu-id="46cd2-112">1:</span></span>
```

```

## <span data-ttu-id="46cd2-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="46cd2-113">PARAMETERS</span></span>

### <span data-ttu-id="46cd2-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="46cd2-114">-Abort</span></span>
<span data-ttu-id="46cd2-115">Bu cmdlet 'in ayrılmış IP adresi geçişini iptal ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

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

### <span data-ttu-id="46cd2-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="46cd2-116">-Commit</span></span>
<span data-ttu-id="46cd2-117">Bu cmdlet 'in ayrılmış IP adresi geçişini başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

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

### <span data-ttu-id="46cd2-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="46cd2-118">-InformationAction</span></span>
<span data-ttu-id="46cd2-119">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="46cd2-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="46cd2-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="46cd2-121">'A</span><span class="sxs-lookup"><span data-stu-id="46cd2-121">Continue</span></span>
- <span data-ttu-id="46cd2-122">Manıza</span><span class="sxs-lookup"><span data-stu-id="46cd2-122">Ignore</span></span>
- <span data-ttu-id="46cd2-123">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="46cd2-123">Inquire</span></span>
- <span data-ttu-id="46cd2-124">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="46cd2-124">SilentlyContinue</span></span>
- <span data-ttu-id="46cd2-125">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="46cd2-125">Stop</span></span>
- <span data-ttu-id="46cd2-126">Biliriz</span><span class="sxs-lookup"><span data-stu-id="46cd2-126">Suspend</span></span>

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

### <span data-ttu-id="46cd2-127">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="46cd2-127">-InformationVariable</span></span>
<span data-ttu-id="46cd2-128">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="46cd2-129">-Prepare</span><span class="sxs-lookup"><span data-stu-id="46cd2-129">-Prepare</span></span>
<span data-ttu-id="46cd2-130">Bu cmdlet 'in geçiş için ayrılmış IP adresini hazırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="46cd2-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="46cd2-131">-Profile</span></span>
<span data-ttu-id="46cd2-132">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="46cd2-133">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="46cd2-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46cd2-134">-Rezervedıpname</span><span class="sxs-lookup"><span data-stu-id="46cd2-134">-ReservedIPName</span></span>
<span data-ttu-id="46cd2-135">Bu cmdlet 'in geçirolduğu ayrılmış IP adresinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="46cd2-136">-Doğrulama</span><span class="sxs-lookup"><span data-stu-id="46cd2-136">-Validate</span></span>
<span data-ttu-id="46cd2-137">Bu cmdlet 'in geçiş için ayrılmış IP adresini doğrulayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="46cd2-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="46cd2-138">-Confirm</span></span>
<span data-ttu-id="46cd2-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="46cd2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46cd2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46cd2-140">-WhatIf</span></span>
<span data-ttu-id="46cd2-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="46cd2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46cd2-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="46cd2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46cd2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46cd2-143">CommonParameters</span></span>
<span data-ttu-id="46cd2-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="46cd2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46cd2-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46cd2-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46cd2-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="46cd2-146">INPUTS</span></span>

## <span data-ttu-id="46cd2-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="46cd2-147">OUTPUTS</span></span>

## <span data-ttu-id="46cd2-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="46cd2-148">NOTES</span></span>

## <span data-ttu-id="46cd2-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="46cd2-149">RELATED LINKS</span></span>

[<span data-ttu-id="46cd2-150">Taşı-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="46cd2-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="46cd2-151">Taşı-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="46cd2-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="46cd2-152">Taşı-AzureService</span><span class="sxs-lookup"><span data-stu-id="46cd2-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="46cd2-153">Taşı-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="46cd2-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="46cd2-154">Taşı-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="46cd2-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


