---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2CBF8DEF-954C-4D9F-B495-C2F76550BC79
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f7e8a7a08ac2793b7e4aeb8615e5fb8fc1f727
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105615"
---
# <span data-ttu-id="d4a9b-101">Get-AzureRoleSize</span><span class="sxs-lookup"><span data-stu-id="d4a9b-101">Get-AzureRoleSize</span></span>

## <span data-ttu-id="d4a9b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a9b-103">Geçerli aboneliğin rol boyutu bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-103">Gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="d4a9b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d4a9b-104">SYNTAX</span></span>

```
Get-AzureRoleSize [[-InstanceSize] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="d4a9b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d4a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a9b-106">**Get-AzureRoleSize** cmdlet 'i geçerli aboneliğin rol boyutu bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-106">The **Get-AzureRoleSize** cmdlet gets the role size information for the current subscription.</span></span>

## <span data-ttu-id="d4a9b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d4a9b-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a9b-108">Örnek 1: rol boyutu bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="d4a9b-108">Example 1: Get role size information</span></span>
```
PS C:\> Get-AzureRoleSize

          InstanceSize               : A6
          RoleSizeLabel              :
          Cores                      : 4
          MemoryInMb                 : 28672
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="d4a9b-109">Bu komut geçerli aboneliğin rol boyutu bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-109">This command gets role size information for the current subscription.</span></span>

### <span data-ttu-id="d4a9b-110">Örnek 2: rol boyutu bilgilerini alma ve rol boyutu adını belirtme</span><span class="sxs-lookup"><span data-stu-id="d4a9b-110">Example 2: Get role size information and specify the role size name</span></span>
```
PS C:\> Get-AzureRoleSize -InstanceSize A7

          InstanceSize               : A7
          RoleSizeLabel              :
          Cores                      : 8
          MemoryInMb                 : 57344
          SupportedByWebWorkerRoles  : True
          SupportedByVirtualMachines : True
          OperationDescription       : Get-AzureRoleSize
          OperationId                : c5ed7b3a-03b3-548d-876b-6688c5b29cce
          OperationStatus            : Succeeded
```

<span data-ttu-id="d4a9b-111">Bu komut belirtilen rol boyutu için rol boyutu bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-111">This command gets role size information for the specified role size.</span></span>

### <span data-ttu-id="d4a9b-112">Örnek 3: tüm Azure hizmetlerindeki tüm sanal makinelerin rol boyutu bilgilerini alma</span><span class="sxs-lookup"><span data-stu-id="d4a9b-112">Example 3: Get role size information for all virtual machines in all of the Azure services</span></span>
```
PS C:\> Get-AzureService | Get-AzureVM | Get-AzureRoleSize
```

<span data-ttu-id="d4a9b-113">Bu komut, tüm Azure hizmetlerindeki tüm sanal makinelerin rol boyutu bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-113">This command gets role size information for all virtual machines in all of the Azure services.</span></span>

## <span data-ttu-id="d4a9b-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d4a9b-114">PARAMETERS</span></span>

### <span data-ttu-id="d4a9b-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="d4a9b-115">-InformationAction</span></span>
<span data-ttu-id="d4a9b-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d4a9b-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="d4a9b-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d4a9b-118">'A</span><span class="sxs-lookup"><span data-stu-id="d4a9b-118">Continue</span></span>
- <span data-ttu-id="d4a9b-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="d4a9b-119">Ignore</span></span>
- <span data-ttu-id="d4a9b-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="d4a9b-120">Inquire</span></span>
- <span data-ttu-id="d4a9b-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="d4a9b-121">SilentlyContinue</span></span>
- <span data-ttu-id="d4a9b-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="d4a9b-122">Stop</span></span>
- <span data-ttu-id="d4a9b-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="d4a9b-123">Suspend</span></span>

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

### <span data-ttu-id="d4a9b-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="d4a9b-124">-InformationVariable</span></span>
<span data-ttu-id="d4a9b-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d4a9b-126">-Instancesize</span><span class="sxs-lookup"><span data-stu-id="d4a9b-126">-InstanceSize</span></span>
<span data-ttu-id="d4a9b-127">Rol boyutu adını belirtir; Örneğin: Extraküçük, küçük, büyük, Extrabüyük, A5, A6, A7.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-127">Specifies the role size name, for example: ExtraSmall, Small, Large, ExtraLarge, A5, A6, A7.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4a9b-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="d4a9b-128">-Profile</span></span>
<span data-ttu-id="d4a9b-129">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d4a9b-130">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4a9b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a9b-131">CommonParameters</span></span>
<span data-ttu-id="d4a9b-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d4a9b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a9b-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4a9b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a9b-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d4a9b-134">INPUTS</span></span>

## <span data-ttu-id="d4a9b-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d4a9b-135">OUTPUTS</span></span>

## <span data-ttu-id="d4a9b-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d4a9b-136">NOTES</span></span>

## <span data-ttu-id="d4a9b-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d4a9b-137">RELATED LINKS</span></span>

[<span data-ttu-id="d4a9b-138">Get-AzureRole</span><span class="sxs-lookup"><span data-stu-id="d4a9b-138">Get-AzureRole</span></span>](./Get-AzureRole.md)

[<span data-ttu-id="d4a9b-139">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="d4a9b-139">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="d4a9b-140">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="d4a9b-140">Get-AzureVM</span></span>](./Get-AzureVM.md)


