---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106243"
---
# <span data-ttu-id="fca89-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fca89-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="fca89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fca89-102">SYNOPSIS</span></span>
<span data-ttu-id="fca89-103">Ağ güvenlik grubunu Azure Resource Manager yığınına geçirir.</span><span class="sxs-lookup"><span data-stu-id="fca89-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="fca89-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fca89-104">SYNTAX</span></span>

### <span data-ttu-id="fca89-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="fca89-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fca89-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="fca89-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fca89-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="fca89-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fca89-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="fca89-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fca89-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="fca89-109">DESCRIPTION</span></span>
<span data-ttu-id="fca89-110">**Taşıma-AzureNetworkSecurityGroup** cmdlet 'i, bir ağ güvenlik grubunu Azure Kaynak Yöneticisi yığınındaki bir kaynak grubuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="fca89-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="fca89-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fca89-111">EXAMPLES</span></span>

### <span data-ttu-id="fca89-112">2</span><span class="sxs-lookup"><span data-stu-id="fca89-112">1:</span></span>
```

```

## <span data-ttu-id="fca89-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fca89-113">PARAMETERS</span></span>

### <span data-ttu-id="fca89-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="fca89-114">-Abort</span></span>
<span data-ttu-id="fca89-115">Bu cmdlet 'in ağ güvenliği grubu geçişini iptal ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="fca89-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="fca89-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="fca89-116">-Commit</span></span>
<span data-ttu-id="fca89-117">Bu cmdlet 'in ağ güvenlik grubu geçişini başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fca89-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="fca89-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="fca89-118">-InformationAction</span></span>
<span data-ttu-id="fca89-119">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fca89-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="fca89-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="fca89-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fca89-121">'A</span><span class="sxs-lookup"><span data-stu-id="fca89-121">Continue</span></span>
- <span data-ttu-id="fca89-122">Manıza</span><span class="sxs-lookup"><span data-stu-id="fca89-122">Ignore</span></span>
- <span data-ttu-id="fca89-123">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="fca89-123">Inquire</span></span>
- <span data-ttu-id="fca89-124">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="fca89-124">SilentlyContinue</span></span>
- <span data-ttu-id="fca89-125">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="fca89-125">Stop</span></span>
- <span data-ttu-id="fca89-126">Biliriz</span><span class="sxs-lookup"><span data-stu-id="fca89-126">Suspend</span></span>

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

### <span data-ttu-id="fca89-127">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="fca89-127">-InformationVariable</span></span>
<span data-ttu-id="fca89-128">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="fca89-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="fca89-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="fca89-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="fca89-130">Bu cmdlet 'in geçirolduğu ağ güvenlik grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fca89-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="fca89-131">-Prepare</span><span class="sxs-lookup"><span data-stu-id="fca89-131">-Prepare</span></span>
<span data-ttu-id="fca89-132">Bu cmdlet 'in geçiş için ağ güvenlik grubunu hazırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fca89-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="fca89-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="fca89-133">-Profile</span></span>
<span data-ttu-id="fca89-134">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="fca89-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fca89-135">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="fca89-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fca89-136">-Doğrulama</span><span class="sxs-lookup"><span data-stu-id="fca89-136">-Validate</span></span>
<span data-ttu-id="fca89-137">Bu cmdlet 'in geçiş için ağ güvenlik grubunu doğrulayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="fca89-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="fca89-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="fca89-138">-Confirm</span></span>
<span data-ttu-id="fca89-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fca89-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fca89-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fca89-140">-WhatIf</span></span>
<span data-ttu-id="fca89-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fca89-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fca89-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fca89-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fca89-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca89-143">CommonParameters</span></span>
<span data-ttu-id="fca89-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fca89-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca89-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fca89-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca89-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fca89-146">INPUTS</span></span>

## <span data-ttu-id="fca89-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fca89-147">OUTPUTS</span></span>

## <span data-ttu-id="fca89-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fca89-148">NOTES</span></span>

## <span data-ttu-id="fca89-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fca89-149">RELATED LINKS</span></span>

[<span data-ttu-id="fca89-150">Taşı-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="fca89-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="fca89-151">Taşı-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="fca89-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="fca89-152">Taşı-AzureService</span><span class="sxs-lookup"><span data-stu-id="fca89-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="fca89-153">Taşı-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fca89-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="fca89-154">Taşı-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fca89-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


