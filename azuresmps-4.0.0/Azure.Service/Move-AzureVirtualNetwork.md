---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106238"
---
# <span data-ttu-id="aa6c6-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="aa6c6-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="aa6c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa6c6-102">SYNOPSIS</span></span>
<span data-ttu-id="aa6c6-103">Sanal ağı Azure Resource Manager yığınına geçirir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="aa6c6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa6c6-104">SYNTAX</span></span>

### <span data-ttu-id="aa6c6-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa6c6-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa6c6-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa6c6-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa6c6-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa6c6-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa6c6-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa6c6-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa6c6-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa6c6-109">DESCRIPTION</span></span>
<span data-ttu-id="aa6c6-110">**Taþý-AzureVirtualNetwork** cmdlet 'ı, Azure Resource Manager yığınındaki bir sanal ağı kaynak grubuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="aa6c6-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa6c6-111">EXAMPLES</span></span>

### <span data-ttu-id="aa6c6-112">Örnek 1: sanal ağ geçişini hazırlama</span><span class="sxs-lookup"><span data-stu-id="aa6c6-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="aa6c6-113">Bu komut, yükseltme için ContosoVNET adındaki sanal ağı Azure Resource Manager yığınına hazırlar.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="aa6c6-114">Örnek 2: sanal ağ geçişini Başlat</span><span class="sxs-lookup"><span data-stu-id="aa6c6-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="aa6c6-115">Bu komut, ContosoVNET adlı sanal ağın Azure Resource Manager yığınına geçirilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="aa6c6-116">Örnek 3: sanal ağ geçişini doğrulama</span><span class="sxs-lookup"><span data-stu-id="aa6c6-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="aa6c6-117">Bu komut, ContosoVNET adlı sanal ağın geçişini Azure Resource Manager yığınına doğrular.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="aa6c6-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa6c6-118">PARAMETERS</span></span>

### <span data-ttu-id="aa6c6-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="aa6c6-119">-Abort</span></span>
<span data-ttu-id="aa6c6-120">Bu cmdlet 'in sanal ağ geçişini iptal ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

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

### <span data-ttu-id="aa6c6-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="aa6c6-121">-Commit</span></span>
<span data-ttu-id="aa6c6-122">Bu cmdlet 'in sanal ağ geçişini başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

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

### <span data-ttu-id="aa6c6-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="aa6c6-123">-InformationAction</span></span>
<span data-ttu-id="aa6c6-124">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="aa6c6-125">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="aa6c6-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="aa6c6-126">'A</span><span class="sxs-lookup"><span data-stu-id="aa6c6-126">Continue</span></span>
- <span data-ttu-id="aa6c6-127">Manıza</span><span class="sxs-lookup"><span data-stu-id="aa6c6-127">Ignore</span></span>
- <span data-ttu-id="aa6c6-128">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="aa6c6-128">Inquire</span></span>
- <span data-ttu-id="aa6c6-129">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="aa6c6-129">SilentlyContinue</span></span>
- <span data-ttu-id="aa6c6-130">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="aa6c6-130">Stop</span></span>
- <span data-ttu-id="aa6c6-131">Biliriz</span><span class="sxs-lookup"><span data-stu-id="aa6c6-131">Suspend</span></span>

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

### <span data-ttu-id="aa6c6-132">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="aa6c6-132">-InformationVariable</span></span>
<span data-ttu-id="aa6c6-133">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="aa6c6-134">-Prepare</span><span class="sxs-lookup"><span data-stu-id="aa6c6-134">-Prepare</span></span>
<span data-ttu-id="aa6c6-135">Bu cmdlet 'in sanal ağı geçiş için hazırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

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

### <span data-ttu-id="aa6c6-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="aa6c6-136">-Profile</span></span>
<span data-ttu-id="aa6c6-137">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="aa6c6-138">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="aa6c6-139">-Doğrulama</span><span class="sxs-lookup"><span data-stu-id="aa6c6-139">-Validate</span></span>
<span data-ttu-id="aa6c6-140">Bu cmdlet 'in geçiş için sanal ağı doğrulayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

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

### <span data-ttu-id="aa6c6-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="aa6c6-141">-VirtualNetworkName</span></span>
<span data-ttu-id="aa6c6-142">Geçirilecek sanal ağın adı</span><span class="sxs-lookup"><span data-stu-id="aa6c6-142">Name of the Virtual Network to migrate</span></span>

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

### <span data-ttu-id="aa6c6-143">-Onay</span><span class="sxs-lookup"><span data-stu-id="aa6c6-143">-Confirm</span></span>
<span data-ttu-id="aa6c6-144">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa6c6-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa6c6-145">-WhatIf</span></span>
<span data-ttu-id="aa6c6-146">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa6c6-147">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa6c6-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa6c6-148">CommonParameters</span></span>
<span data-ttu-id="aa6c6-149">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa6c6-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa6c6-150">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa6c6-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa6c6-151">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa6c6-151">INPUTS</span></span>

## <span data-ttu-id="aa6c6-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa6c6-152">OUTPUTS</span></span>

## <span data-ttu-id="aa6c6-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa6c6-153">NOTES</span></span>

## <span data-ttu-id="aa6c6-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa6c6-154">RELATED LINKS</span></span>

[<span data-ttu-id="aa6c6-155">Taşı-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="aa6c6-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="aa6c6-156">Taşı-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="aa6c6-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="aa6c6-157">Taşı-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="aa6c6-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="aa6c6-158">Taşı-AzureService</span><span class="sxs-lookup"><span data-stu-id="aa6c6-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="aa6c6-159">Taşı-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="aa6c6-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


