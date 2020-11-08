---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106240"
---
# <span data-ttu-id="a911d-101">Move-AzureService</span><span class="sxs-lookup"><span data-stu-id="a911d-101">Move-AzureService</span></span>

## <span data-ttu-id="a911d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a911d-102">SYNOPSIS</span></span>
<span data-ttu-id="a911d-103">Bulut hizmetini Azure Kaynak Yöneticisi yığınına geçirir.</span><span class="sxs-lookup"><span data-stu-id="a911d-103">Migrates a cloud service to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a911d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a911d-104">SYNTAX</span></span>

### <span data-ttu-id="a911d-105">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a911d-105">AbortMigrationParameterSet</span></span>
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a911d-106">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a911d-106">CommitMigrationParameterSet</span></span>
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a911d-107">Örnek ayarlama</span><span class="sxs-lookup"><span data-stu-id="a911d-107">PrepareNewMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a911d-108">PrepareExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a911d-108">PrepareExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a911d-109">ValidateNewMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a911d-109">ValidateNewMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a911d-110">ValidateExistingMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="a911d-110">ValidateExistingMigrationParameterSet</span></span>
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a911d-111">Tanım</span><span class="sxs-lookup"><span data-stu-id="a911d-111">DESCRIPTION</span></span>
<span data-ttu-id="a911d-112">**Taþý-AzureService** cmdlet 'i bir bulut hizmetini ve bu hizmetin içindeki bir dağıtımı Azure Resource Manager yığınındaki bir kaynak grubuna geçirir.</span><span class="sxs-lookup"><span data-stu-id="a911d-112">The **Move-AzureService** cmdlet migrates a cloud service and a deployment inside that service to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="a911d-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a911d-113">EXAMPLES</span></span>

### <span data-ttu-id="a911d-114">Örnek 1: hizmet geçişini hazırlama</span><span class="sxs-lookup"><span data-stu-id="a911d-114">Example 1: Prepare service migration</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="a911d-115">Bu komut, Azure Resource Manager yığınına geçiş için ContosoService adındaki hizmeti hazırlar.</span><span class="sxs-lookup"><span data-stu-id="a911d-115">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a911d-116">Geçiş, ContosoVM adlı dağıtımı içerir.</span><span class="sxs-lookup"><span data-stu-id="a911d-116">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="a911d-117">Örnek 2: hizmet geçişini başlatma</span><span class="sxs-lookup"><span data-stu-id="a911d-117">Example 2: Start service migration</span></span>
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="a911d-118">Bu komut, ContosoService adlı hizmetin Azure Resource Manager yığınına geçirilmesini başlatır.</span><span class="sxs-lookup"><span data-stu-id="a911d-118">This command starts migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a911d-119">Geçiş, ContosoVM adlı dağıtımı içerir.</span><span class="sxs-lookup"><span data-stu-id="a911d-119">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="a911d-120">Örnek 3: hizmet geçişini Iptal etme</span><span class="sxs-lookup"><span data-stu-id="a911d-120">Example 3: Cancel service migration</span></span>
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

<span data-ttu-id="a911d-121">Bu komut, ContosoService adlı hizmetin Azure Resource Manager yığınına geçirilmesini iptal eder.</span><span class="sxs-lookup"><span data-stu-id="a911d-121">This command cancels migration of the service named ContosoService to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="a911d-122">Örnek 4: varolan sanal ağa hizmet geçişi hazırlama</span><span class="sxs-lookup"><span data-stu-id="a911d-122">Example 4: Prepare service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

<span data-ttu-id="a911d-123">Bu komut, Azure Resource Manager yığınına geçiş için ContosoService adındaki hizmeti hazırlar.</span><span class="sxs-lookup"><span data-stu-id="a911d-123">This command prepares the service named ContosoService for migration to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a911d-124">Geçiş, ContosoVM adlı dağıtımı içerir.</span><span class="sxs-lookup"><span data-stu-id="a911d-124">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="a911d-125">Geçiş, önceden oluşturulmuş bir sanal ağı kullanır.</span><span class="sxs-lookup"><span data-stu-id="a911d-125">The migration uses a virtual network that was previously created.</span></span>

### <span data-ttu-id="a911d-126">Örnek 5: hizmet geçişini doğrulama</span><span class="sxs-lookup"><span data-stu-id="a911d-126">Example 5: Validate service migration</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

<span data-ttu-id="a911d-127">Bu komut, ContosoService adındaki hizmetin geçişini Azure Resource Manager yığınına doğrular.</span><span class="sxs-lookup"><span data-stu-id="a911d-127">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a911d-128">Geçiş, ContosoVM adlı dağıtımı içerir.</span><span class="sxs-lookup"><span data-stu-id="a911d-128">The migration includes the deployment named ContosoVM.</span></span>

### <span data-ttu-id="a911d-129">Örnek 6: mevcut sanal ağa yönelik hizmet geçişini doğrulama</span><span class="sxs-lookup"><span data-stu-id="a911d-129">Example 6: Validate service migration to an existing virtual network</span></span>
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

<span data-ttu-id="a911d-130">Bu komut, ContosoService adındaki hizmetin geçişini Azure Resource Manager yığınına doğrular.</span><span class="sxs-lookup"><span data-stu-id="a911d-130">This command validates migration for the service named ContosoService to the Azure Resource Manager stack.</span></span>
<span data-ttu-id="a911d-131">Geçiş, ContosoVM adlı dağıtımı içerir.</span><span class="sxs-lookup"><span data-stu-id="a911d-131">The migration includes the deployment named ContosoVM.</span></span>
<span data-ttu-id="a911d-132">Geçiş, önceden oluşturulmuş bir sanal ağı kullanır.</span><span class="sxs-lookup"><span data-stu-id="a911d-132">The migration uses a virtual network that was previously created.</span></span>

## <span data-ttu-id="a911d-133">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a911d-133">PARAMETERS</span></span>

### <span data-ttu-id="a911d-134">-Abort</span><span class="sxs-lookup"><span data-stu-id="a911d-134">-Abort</span></span>
<span data-ttu-id="a911d-135">Bu cmdlet 'in hizmet geçişini iptal ettiğini gösterir.</span><span class="sxs-lookup"><span data-stu-id="a911d-135">Indicates that this cmdlet cancels the service migration.</span></span>

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

### <span data-ttu-id="a911d-136">-Commit</span><span class="sxs-lookup"><span data-stu-id="a911d-136">-Commit</span></span>
<span data-ttu-id="a911d-137">Bu cmdlet 'in hizmet geçişini başlattığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a911d-137">Indicates that this cmdlet starts the service migration.</span></span>

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

### <span data-ttu-id="a911d-138">-CreateNewVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a911d-138">-CreateNewVirtualNetwork</span></span>
<span data-ttu-id="a911d-139">Bu cmdlet 'in Azure Resource Manager yığınında sanal ağ oluşturduğunu gösterir.</span><span class="sxs-lookup"><span data-stu-id="a911d-139">Indicates that this cmdlet creates a virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a911d-140">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="a911d-140">-DeploymentName</span></span>
<span data-ttu-id="a911d-141">Bu cmdlet 'in geçirolduğu bulut hizmeti dağıtımının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-141">Specifies the name of the cloud service deployment that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a911d-142">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a911d-142">-InformationAction</span></span>
<span data-ttu-id="a911d-143">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-143">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a911d-144">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a911d-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a911d-145">'A</span><span class="sxs-lookup"><span data-stu-id="a911d-145">Continue</span></span>
- <span data-ttu-id="a911d-146">Manıza</span><span class="sxs-lookup"><span data-stu-id="a911d-146">Ignore</span></span>
- <span data-ttu-id="a911d-147">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="a911d-147">Inquire</span></span>
- <span data-ttu-id="a911d-148">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="a911d-148">SilentlyContinue</span></span>
- <span data-ttu-id="a911d-149">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="a911d-149">Stop</span></span>
- <span data-ttu-id="a911d-150">Biliriz</span><span class="sxs-lookup"><span data-stu-id="a911d-150">Suspend</span></span>

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

### <span data-ttu-id="a911d-151">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="a911d-151">-InformationVariable</span></span>
<span data-ttu-id="a911d-152">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-152">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a911d-153">-Prepare</span><span class="sxs-lookup"><span data-stu-id="a911d-153">-Prepare</span></span>
<span data-ttu-id="a911d-154">Bu cmdlet 'in, yükseltme için bulut hizmetini hazırtığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a911d-154">Indicates that this cmdlet prepares the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a911d-155">-Profil</span><span class="sxs-lookup"><span data-stu-id="a911d-155">-Profile</span></span>
<span data-ttu-id="a911d-156">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-156">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a911d-157">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a911d-157">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a911d-158">-HizmetAdı</span><span class="sxs-lookup"><span data-stu-id="a911d-158">-ServiceName</span></span>
<span data-ttu-id="a911d-159">Bu cmdlet 'in geçirolduğu bulut hizmetinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-159">Specifies the name  of the cloud service that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="a911d-160">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="a911d-160">-SubnetName</span></span>
<span data-ttu-id="a911d-161">Sanal ağ içindeki alt ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-161">Specifies the name of the Subnet inside the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a911d-162">-UseExistingVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a911d-162">-UseExistingVirtualNetwork</span></span>
<span data-ttu-id="a911d-163">Bu cmdlet 'in bulut hizmetini Azure Resource Manager yığınında var olan bir sanal ağa geçirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-163">Indicates that this cmdlet migrates the cloud service to an existing virtual network in the Azure Resource Manager stack.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a911d-164">-Doğrulama</span><span class="sxs-lookup"><span data-stu-id="a911d-164">-Validate</span></span>
<span data-ttu-id="a911d-165">Bu cmdlet 'in geçiş için bulut hizmetini doğrulayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-165">Specifies that this cmdlet validates the cloud service for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a911d-166">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="a911d-166">-VirtualNetworkName</span></span>
<span data-ttu-id="a911d-167">Sanal ağın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-167">Specifies the name of a virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a911d-168">-VirtualNetworkResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a911d-168">-VirtualNetworkResourceGroupName</span></span>
<span data-ttu-id="a911d-169">Var olan bir sanal ağın kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a911d-169">Specifies the name of the resource group of an existing virtual network.</span></span>

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a911d-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a911d-170">CommonParameters</span></span>
<span data-ttu-id="a911d-171">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a911d-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a911d-172">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a911d-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a911d-173">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a911d-173">INPUTS</span></span>

## <span data-ttu-id="a911d-174">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a911d-174">OUTPUTS</span></span>

## <span data-ttu-id="a911d-175">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a911d-175">NOTES</span></span>

## <span data-ttu-id="a911d-176">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a911d-176">RELATED LINKS</span></span>

[<span data-ttu-id="a911d-177">Taşı-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a911d-177">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="a911d-178">Taşı-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="a911d-178">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="a911d-179">Taşı-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="a911d-179">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="a911d-180">Taşı-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="a911d-180">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="a911d-181">Taşı-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a911d-181">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


